# How to connect Github Pages to Custom Domain

Tutorial of linking Github Pages to Custom Domain.

<!--more-->

## Intro
This is showing how to link Github Pages to a Custom Domain, we are using namecheap here. Others, e.g. GoDaddy… can apply the same method.

## Steps:
1. Buy a domain
2. In Github repository Settings, then Click Page, add the domain you purchased to the ‘Custom domain box’ (no ‘www’)
3. Enforce HTTPS (Github) (Optional)
4. Go Dashboard (make sure NAMESERVERS of the domain is set to Basic DNS)
5. Click ‘Mange’ button of the domain name you choose
6. Click Advanced DNS
7. For the HOST RECORDS, Add new records
    - Type = CNAME * 1
        - Host = www
        - Value = username.github.io
        - TTL = Automatic
    - Type = A Records(@) * 4
        - Host = @
        - Value = 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
        - TTL = Automatic

    Values might have changed since the time of writing. Check [offical docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain) for the most up-to-date values.

8. Remove old Records
9. Done. Visit to the domain and be patient!

