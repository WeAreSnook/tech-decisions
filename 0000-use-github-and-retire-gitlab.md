# Use Github and retire Gitlab

## Context

### Gitlab

When setting up the team, we initially used Gitlab for version control. This decision was taken as Gitlab offered:

- free private repositories
- an integrated CI/CD framework

One requirement of some work we were doing for NPS (our parent company) was to deploy the code within their private network.

To facilitate the smooth transition of code from our repositories to our servers, we moved Gitlab from an externally hosted solution into one that we hosted ourselves within the NPS network and behind a VPN.

Our Gitlab install is currently available at http://code.snook when connected to Snook's VPN.

This has created barriers for onboarding new team members. People need a VPN account created before they could access code.

Additionally, our VPN connection with NPS is unstable. This has had negative impacts on the team's productivity.

### Github

We recently set up a new Github account available at https://github.com/wearesnook

Github shares a feature set with Gitlab, but enjoys more market share and as such is seen as a first-class citizen for any application that wants to interface with a version control system.

It does not need VPN access to view issues or submit code.

## Decision

All new projects should be created under Snook's Github organisation. We will retire use of Gitlab.Gitlab will temporarily be used for hosting code for NPS projects that require access to their networks. After this we will look to retire use of Gitlab completely.

## Status

Accepted

## Consequences

### Pros

Github is known as a social code platform and is arguably the platform for sharing open source code. Hosting our code on Github helps us build a technical identity and share our work. Having a cloud based version control system means we can rapidly onboard people to projects, without VPN access.

We were paying for use of Gitlab's more advanced features. By moving to Github, we save a significant monthly cost that can be better invested in other resources for the team.

### Cons

We had previously been using Gitlab's CI/CD tooling. This means that we have to evaluate new CI/CD tools for the team and make sure our team has sufficient training with CI/CD.
