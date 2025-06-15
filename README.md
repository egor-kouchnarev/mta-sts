# Host MTA-STS policy with GitHub Pages

---

### 1. Create repository

* Open **[egor-kouchnarev/mta-sts](https://github.com/egor-kouchnarev/mta-sts)** and select **Create a new repository** from the **Use this template** dropdown on the top right.
* Enter a **name**, and leave visibility as **Public** (GitHub Pages is only available in public repositories with GitHub Free and GitHub Free for organisations plans).
* Click **Create Repository**.

### 2. Host repository

* Open **Settings**, then, in the left select **Pages** (under **Code and automation**).
* Select **Main** from the dropdown list under **Branch**.
* Click **Save**.

### 3. Publish DNS records

* `mta-sts.<EXAMPLE.TEST>.	300	IN	CNAME	<GITHUB-USERNAME>.github.io.`
* `_mta-sts.<EXAMPLE.TEST>. 300	IN	TXT	"v=STSv1; id=<UNIQUE-IDENTIFIER>"`

### 4. Configure custom domain and TLS
 
* Enter *mta-sts.<domain>* in the **Custom Domain** field.
* Once the **DNS Check** completes, Select **Enforce HTTPS**.

---

## References

* https://github.com/jpawlowski/mta-sts.template
* https://github.com/orgs/community/discussions/22227#discussioncomment-3235986
* https://docs.github.com/en/pages/
  *  https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
  *  https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages
  * https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https
  *  https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits
* https://datatracker.ietf.org/doc/html/rfc8461 
  * https://datatracker.ietf.org/doc/html/rfc8461#section-8.2
