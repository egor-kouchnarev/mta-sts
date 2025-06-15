# Hosted MTA-STS policy on GitHub Pages

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus consequat et lacus volutpat laoreet. Nam venenatis tortor non urna elementum mattis. Curabitur mollis felis id risus lacinia aliquam vulputate nec massa. Sed porttitor tincidunt vulputate. Maecenas varius dolor velit, ac interdum justo egestas eget. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; In at elit nec ligula maximus malesuada.

# Usage

Donec eget nisi ac sapien cursus maximus. Nullam id placerat sem. Fusce sed mi maximus, aliquam libero quis, viverra tortor. Vivamus laoreet nisi a velit condimentum viverra. Vivamus malesuada convallis enim, eu fringilla ipsum dignissim vitae. In hac habitasse platea dictumst. Duis elementum scelerisque arcu, eget iaculis nisl posuere ac.

### Create repository

1. Create a new repository from the [github.com/egor-kouchnarev/mta-sts](https://github.com/egor-kouchnarev/mta-sts) template.
2. Set visibulity to _Public_ if using Free GitHub plan.
3. Edit the `./well-known/**mta-sts.txt**` policy file to reflect your configuration.

### Configure GitHub Pages

4. ...
5. ...
6. ...

### Publish DNS records

7. Publish a CNAME record in your domain DNS zone: `mta-sts.**<domain>**.	300	IN	CNAME	**<github-account-name>**.github.io.`.
8. Publish a TXT record in your domain DNS zone: `_mta-sts.kouchnarev.com. 300	IN	TXT	"v=STSv1; id=**<unique-identifier>**"`.

### Configure GitHub Pages
 
9. Enter `mta-sts.**<domain>**` in the _Custom Domain_ field.
10. Check _Enforce HTTPS_.





Nulla consectetur in metus vitae molestie. Integer fringilla urna at faucibus accumsan. Donec varius vulputate purus, sit amet rhoncus orci pharetra vitae. Nunc ut ligula eget neque tincidunt fermentum. Pellentesque suscipit tortor eu lacus iaculis, at fringilla dolor faucibus. Mauris porta egestas purus, a consequat dui porttitor ut. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Phasellus pulvinar dictum ante id luctus. Sed porttitor ullamcorper sapien, at maximus enim facilisis eu. Pellentesque consectetur ex risus, nec dapibus turpis ultrices ut.

Donec eget nisi ac sapien cursus maximus. Nullam id placerat sem. Fusce sed mi maximus, aliquam libero quis, viverra tortor. Vivamus laoreet nisi a velit condimentum viverra. Vivamus malesuada convallis enim, eu fringilla ipsum dignissim vitae. In hac habitasse platea dictumst. Duis elementum scelerisque arcu, eget iaculis nisl posuere ac.

Quisque mollis eros mi, a blandit lacus lacinia vel. Quisque in libero quis ante imperdiet sodales id vitae justo. Proin finibus, urna at consequat malesuada, turpis eros ullamcorper urna, eu semper tellus velit eu dolor. Duis vel justo finibus, posuere nunc in, lobortis purus. Vivamus sed massa at libero tempus ultrices a venenatis dolor. Aenean fringilla nulla et eros dignissim, quis vestibulum ex dignissim. Curabitur laoreet, metus sit amet tristique eleifend, tortor dolor cursus magna, ac pellentesque libero urna sed nisi. Ut malesuada arcu commodo, rutrum justo eget, pulvinar leo. Proin scelerisque ullamcorper lorem suscipit eleifend. Vivamus nunc metus, faucibus sed rutrum et, blandit ut dolor. Aliquam egestas arcu nec ligula mattis porta. Nullam vehicula porta lacus, in malesuada eros posuere at.
