# Hosted MTA-STS policy with GitHub Pages

Donec eget nisi ac sapien cursus maximus. Nullam id placerat sem. Fusce sed mi maximus, aliquam libero quis, viverra tortor. Vivamus laoreet nisi a velit condimentum viverra. Vivamus malesuada convallis enim, eu fringilla ipsum dignissim vitae. In hac habitasse platea dictumst. Duis elementum scelerisque arcu, eget iaculis nisl posuere ac.

# Steps

### Create repository

1. Create a new repository from the [github.com/egor-kouchnarev/mta-sts](https://github.com/egor-kouchnarev/mta-sts) template
2. Enter a repository name, and Set visibility to **Public** if using Free GitHub plan
3. Edit the *./well-known/mta-sts.txt* policy file to reflect your configuration

### Host repository

4. Open **Settings**, then, in the side menu select **Pages** (under **Code and automation**)
5. Select **Main** from the drop-down list under **Branch**, then click **Save**

### Publish DNS records

7. `mta-sts.<domain>.	300	IN	CNAME	<github-account-name>.github.io.`
8. `_mta-sts.kouchnarev.com. 300	IN	TXT	"v=STSv1; id=<unique-identifier>"`

### Configure custom domain and TLS
 
9. Enter *mta-sts.<domain>* in the **Custom Domain** field
10. Once the **DNS Check** completes, Check **Enforce HTTPS**

### Verify

* `curl "https://mta-sts.<domain>/.well-known/mta-sts.txt"`
* `dig _mta-sts.<domain> txt`

## References

* https://github.com/jpawlowski/mta-sts.template
* https://github.com/orgs/community/discussions/22227#discussioncomment-3235986
* https://docs.github.com/en/pages/
  *  https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
  *  https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages
  * https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https
  *  https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits
* https://datatracker.ietf.org/doc/html/rfc8461 https://datatracker.ietf.org/doc/html/rfc8461#section-8.2
