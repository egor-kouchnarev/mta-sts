# Heading 1

Donec eget nisi ac sapien cursus maximus. Nullam id placerat sem. Fusce sed mi maximus, aliquam libero quis, viverra tortor. Vivamus laoreet nisi a velit condimentum viverra. Vivamus malesuada convallis enim, eu fringilla ipsum dignissim vitae. In hac habitasse platea dictumst. Duis elementum scelerisque arcu, eget iaculis nisl posuere ac.

# Steps

### Create repository

1. Create a new repository from the [github.com/egor-kouchnarev/mta-sts](https://github.com/egor-kouchnarev/mta-sts) template.
2. Enter a repository name, and Set visibility to _Public_ if using Free GitHub plan.
3. Edit the `./well-known/mta-sts.txt` policy file to reflect your configuration.

### Host repository

4. Open _Settings_, then, in the side menu select _Pages_ (under _Code and automation_).
5. Select _Main_ from the drop-down list under _Branch_, then click _Save_.

### Publish DNS records

7. CNAME: `mta-sts.<domain>.	300	IN	CNAME	<github-account-name>.github.io.`.
8. TXT: `_mta-sts.kouchnarev.com. 300	IN	TXT	"v=STSv1; id=<unique-identifier>"`.

### Configure custom domain and TLS
 
9. Enter `mta-sts.<domain>` in the _Custom Domain_ field.
10. Check _Enforce HTTPS_.

### Verify

Donec varius vulputate purus, sit amet rhoncus orci pharetra vitae. Nunc ut ligula eget neque tincidunt fermentum.

* `curl "https://mta-sts.<domain>/.well-known/mta-sts.txt"`
* `dig _mta-sts.<domain> txt`

# Heading 2

Nulla consectetur in metus vitae molestie. Integer fringilla urna at faucibus accumsan. Donec varius vulputate purus, sit amet rhoncus orci pharetra vitae. Nunc ut ligula eget neque tincidunt fermentum. Pellentesque suscipit tortor eu lacus iaculis, at fringilla dolor faucibus. Mauris porta egestas purus, a consequat dui porttitor ut. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Phasellus pulvinar dictum ante id luctus. Sed porttitor ullamcorper sapien, at maximus enim facilisis eu. Pellentesque consectetur ex risus, nec dapibus turpis ultrices ut.

## References

* https://github.com/jpawlowski/mta-sts.template
* https://github.com/orgs/community/discussions/22227#discussioncomment-3235986
* https://docs.github.com/en/pages/
  *  https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
  *  https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages
  * https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https
  *  https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits
* https://datatracker.ietf.org/doc/html/rfc8461 https://datatracker.ietf.org/doc/html/rfc8461#section-8.2
