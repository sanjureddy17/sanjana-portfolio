# DNS Walkthrough – Personal Portfolio

## What is DNS?

DNS (Domain Name System) translates a human-readable domain name into the information needed to reach the correct server. Instead of remembering an IP address, users can type a domain name such as `sanjana-portfolio-ashen.vercel.app`.

When someone enters a domain name in a browser, the DNS system helps the browser find where that website is hosted.

## What is a CNAME record?

A CNAME (Canonical Name) record is a DNS record that points one domain name to another domain name.

For example, when my FlyRank subdomain is provided, a CNAME record could be used for:

`www.sanjana.flyrank.ai`

The CNAME value would be the target hostname provided by the hosting platform, such as the hostname Vercel gives for the configured custom domain.

A CNAME does not directly contain the website itself. It tells DNS where the requested hostname should point.

## What happens when someone enters my website address?

When someone types my domain into a browser, several steps happen:

1. The browser checks whether it already knows the address from its cache.
2. If it does not, the request goes to a DNS resolver, usually provided by the user's internet service provider or another DNS service.
3. The resolver looks for the DNS information for the requested domain.
4. The resolver communicates with the appropriate authoritative nameserver.
5. The nameserver returns the relevant DNS record, such as a CNAME or A record.
6. The resolver gives the result back to the user's device.
7. The browser uses that information to connect to the hosting platform.
8. The hosting platform returns the website files to the browser.
9. HTTPS encrypts the connection between the browser and the website.

This process usually happens very quickly, so the user normally only sees the website loading.

## What I will do when my FlyRank subdomain is provided

After my FlyRank capstone is approved, I will receive a subdomain such as:

`my assigned FlyRank subdomain`

FlyRank Ops will create the required DNS record for the subdomain.

I will then:

1. Add the FlyRank subdomain as a custom domain in my hosting platform.
2. Configure the domain according to the DNS value provided by the hosting platform.
3. Wait for DNS changes to propagate.
4. Verify that the domain points to my existing portfolio.
5. Confirm that the website loads over HTTPS and that the browser shows the padlock.

The existing website does not need to be rebuilt. The custom domain simply points to the website that is already hosted.

## Summary

DNS acts like the Internet's addressing system. A CNAME record allows one hostname to point to another hostname. When my FlyRank subdomain is provisioned, I will connect that domain to my existing hosted portfolio, wait for DNS propagation, and verify HTTPS. This means the domain changes while the underlying website remains the same.
