# Host MTA-STS policy with GitHub Pages

## Instructions

### Create repository

* Open **[egor-kouchnarev/mta-sts](https://github.com/egor-kouchnarev/mta-sts)** and select **Create a new repository** from the **Use this template** dropdown on the top right.
* Enter a **name**, and leave visibility as **Public**(GitHub Pages is only available in public repositories on Free plans).
* Click **Create Repository**.

### Host repository

* In repository **Settings**, click **Pages** (under **Code and automation** in the left menu).
* Select **Main** from the dropdown list under **Branch**.
* Click **Save**.

### Publish DNS records

* `mta-sts.<EXAMPLE.TEST>.	300	IN	CNAME	<GITHUB-USERNAME>.github.io.`
* `_mta-sts.<EXAMPLE.TEST>. 300	IN	TXT	"v=STSv1; id=<UNIQUE-IDENTIFIER>"`

### Enable custom domain
 
* Enter *mta-sts.<EXAMPLE.TEST>* in the **Custom Domain** field.
* When the **DNS Check** has completed, select **Enforce HTTPS**.

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
