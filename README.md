## Hosted MTA-STS policy with GitHub Pages

Donec eget nisi ac sapien cursus maximus. Nullam id placerat sem. Fusce sed mi maximus, aliquam libero quis, viverra tortor. Vivamus laoreet nisi a velit condimentum viverra. Vivamus malesuada convallis enim, eu fringilla ipsum dignissim vitae. In hac habitasse platea dictumst. Duis elementum scelerisque arcu, eget iaculis nisl posuere ac.

---

### Steps

#### Create repository

* Open [egor-kouchnarev/mta-sts](https://github.com/egor-kouchnarev/mta-sts), and select **Create a new repository** from the **Use this template** dropdown on the top right.
* Enter a **name**, and leave visibility as **Public** (GitHub Pages is available in public repositories with GitHub Free and GitHub Free for organisations).
* Click **Create Repository**.

#### Host repository

* Open **Settings**, then, in the left select **Pages** (under **Code and automation**).
* Select **Main** from the dropdown list under **Branch**.
* Click **Save**.

#### Publish DNS records

* `mta-sts.<EXAMPLE.TEST>.	300	IN	CNAME	<GITHUB-USERNAME>.github.io.`
* `_mta-sts.<EXAMPLE.TEST>. 300	IN	TXT	"v=STSv1; id=<UNIQUE-IDENTIFIER>"`

#### Configure custom domain and TLS
 
* Enter *mta-sts.<domain>* in the **Custom Domain** field.
* Once the **DNS Check** completes, Select **Enforce HTTPS**.

#### Verify

* `curl "https://mta-sts.<EXAMPLE.TEST>/.well-known/mta-sts.txt"`
* `dig _mta-sts.<EXAMPLE.TEST> txt`

---

### References

* https://github.com/jpawlowski/mta-sts.template
* https://github.com/orgs/community/discussions/22227#discussioncomment-3235986
* https://docs.github.com/en/pages/
  *  https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
  *  https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages
  * https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https
  *  https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits
* https://datatracker.ietf.org/doc/html/rfc8461 https://datatracker.ietf.org/doc/html/rfc8461#section-8.2
