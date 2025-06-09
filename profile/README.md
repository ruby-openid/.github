
[![Liberapay Goal Progress][⛳liberapay-img]][⛳liberapay] [![Sponsor Me on Github][🖇sponsor-img]][🖇sponsor] [![Buy me a coffee][🖇buyme-small-img]][🖇buyme] [![Donate on Polar][🖇polar-img]][🖇polar] [![Donate to my FLOSS or refugee efforts at ko-fi.com][🖇kofi-img]][🖇kofi] [![Donate to my FLOSS or refugee efforts using Patreon][🖇patreon-img]][🖇patreon]


NOTE: OpenID v2 is *not* OpenID Connect (OIDC).  OpenID v2, finalized in 2007, is the predecessor standard. OIDC, which began formulation in 2011, is the successor standard. OpenID v2 is *not* based on OAuth 2, while OIDC is.  OAuth 2 didn't even exist when OpenID v2 was finalized.  Both OpenID v2 and OIDC  standards are governed by OpenID.net.  And with that out of the way...

I recently assumed the maintainer role for the [omniauth-openid](https://github.com/ruby-openid/omniauth-openid) gem, and a new patch release is out now, the first in several years. The primary purpose of the release is to prepare users for the next release, which will be a major version bump.

Before delving further into the new release though...

# Why?

Why maintain gems based on ancient standards? Is anyone using them?

Actually, yes. This gem, despite lack of maintenance, and dependencies that have many issues running on modern Ruby, has _only ever grown in daily downloads_, currently around 10,000 per week, which places it firmly in the top 5,000* gems by daily downloads. Some organizations like old standards because they are stable; they literally will not change. As a result, the software supporting the old standards is fairly stable. Others are maintaining old entrenched software which is expensive to replace.  Occasionally new tools need to integrate with those existing tools, and thus the gem's installed base keeps growing.

[![Downloads Rank][👽dl-ranki]][👽dl-rank]

[👽dl-rank]: https://rubygems.org/gems/omniauth-openid
[👽dl-ranki]: https://img.shields.io/gem/rd/omniauth-openid.png

# New in v2.0.2

As is often the case for gems that started life decades ago, there was no declared minimum ruby version.  However, the ancient Travis CI test suite ran against Ruby 2.4 and greater, so it seems fair to assume ruby 2.4 as the de facto minimum ruby version.

A new basic server / client example is available in the gem's source repo at `/examples`.

GitHub Actions provides continuous integration. A vast test matrix covering all supported Ruby engines, and all supported minor versions of omniauth ensures release quality.

`omniauth-openid` version 2.0.2 supports:
- MRI v2: 2.4, 2.5, 2.6, 2.7
- MRI v3: 3.0, 3.1, 3.2, 3.3, 3.4, HEAD
- JRuby 9k: 9.2, 9.3
- JRuby 10k: 10.0, HEAD
- omniauth v1: 1.1, 1.2, 1.3, 1.4, 1.5, 1.6, 1.7, 1.8, 1.9
- omniauth v2: 2.0, 2.1, HEAD

# Coming in v3.0.0

omniauth-openid version 3.0.0, which I expect to release soon, will:
- switch from dead tools to living tools
  - [rack-openid](https://github.com/grosser/rack-openid) (dead for 12 years) &rarr; [rack-openid2](https://github.com/ruby-openid/rack-openid2) (rewritten, modernized, drop-in-replacement)
  - [ruby-openid](https://github.com/openid/ruby-openid) (archived & dead for 6 years) &rarr; [ruby-openid2](https://github.com/ruby-openid/ruby-openid2) (rewritten, modernized, drop-in-replacement)
  - NOTE: these `*-openid2` gems were created by me to underpin my refactored and fully modernized [open_id_authentication](https://github.com/ruby-openid/open_id_authentication) gem, the rewritten, modernized [masq2](https://github.com/ruby-openid/masq2) (OpenID Server Rails Engine) gem, and the rewritten, modernized [rots](https://github.com/ruby-openid/rots) (Ruby OpenID Test Server) gem
- drop support for MRI Ruby 2.4, 2.5. 2.6
- drop support for JRuby 9.2, 9.3

# Outro

Use [my gems](https://rubygems.org/profiles/pboling)?

I'd love to hear about it, so please join my discord.

[![Live Chat on Discord][✉️discord-invite-img]][✉️discord-invite]

[✉️discord-invite]: https://discord.gg/3qme4XHNKN
[✉️discord-invite-img]: https://raster.shields.io/discord/1373797679469170758?style=for-the-badge

Remember to star repos you use, and donate to the open source maintainers. I know there are some large companies using these OpenID tools I've put hundreds of hours of work into... Toss a coin to your witcher.  Thank you!

[![Liberapay Goal Progress][⛳liberapay-img]][⛳liberapay] [![Sponsor Me on Github][🖇sponsor-img]][🖇sponsor] [![Buy me a coffee][🖇buyme-small-img]][🖇buyme] [![Donate on Polar][🖇polar-img]][🖇polar] [![Donate to my FLOSS or refugee efforts at ko-fi.com][🖇kofi-img]][🖇kofi] [![Donate to my FLOSS or refugee efforts using Patreon][🖇patreon-img]][🖇patreon]

[⛳liberapay-img]: https://raster.shields.io/liberapay/goal/pboling.png?logo=liberapay
[⛳liberapay]: https://liberapay.com/pboling/donate
[🖇sponsor-img]: https://raster.shields.io/badge/Sponsor_Me!-pboling.png?style=social&logo=github
[🖇sponsor]: https://github.com/sponsors/pboling
[🖇polar-img]: https://raster.shields.io/badge/polar-donate-yellow.png
[🖇polar]: https://polar.sh/pboling
[🖇kofi-img]: https://raster.shields.io/badge/a_more_different_coffee-✓-yellow.png
[🖇kofi]: https://ko-fi.com/O5O86SNP4
[🖇patreon-img]: https://raster.shields.io/badge/patreon-donate-yellow.png
[🖇patreon]: https://patreon.com/galtzo
[🖇buyme]: https://www.buymeacoffee.com/pboling
[🖇buyme-small-img]: https://raster.shields.io/badge/buy_me_a_coffee-✓-yellow.png?style=flat

If you're hiring for an expert Rubyist let me know.