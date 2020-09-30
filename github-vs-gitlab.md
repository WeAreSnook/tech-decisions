#Github vs Gitlab

We use both Github and Gitlab at Snook, why?

## Gitlab

Our Gitlab install is available at http://code.snook

One of the requirements of some work we were doing for NPS (our parent company) was that the code was deployed within their private network.

To facilitate the smooth transition of code from our repositories to our servers, we moved Gitlab from an externally hosted solution into one that we hosted ourselves within our network and behind a VPN.

This has the knock on effect of build team members needing VPN access to view tickets or submit code.

The VPN is often down so this isn't ideal.

## Github

Our Github account is available at https://github.com/wearesnook

Github shares a feature set with Gitlab, but enjoys more market share and as such is seen as a first-class citizen for any application that wants to interface with a version control system.

It does not need VPN access in order to view issues or submit code.

## When to use each

When deciding between the two:

- When the code being stored needs to be deployed to our internal network, use Gitlab
- When the code being stored does not have the above requirement, use Github
