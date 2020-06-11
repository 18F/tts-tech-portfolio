---
name: Decommissioning
about: Checklist for shutting down a system
title: "decommission [system]"
labels: ""
assignees: ""
---

_Add/remove items, as applicable._

- [ ] Notify any users of the system, via banner across the site, email, Slack, etc. Ideally, help them find alternatives, make sure they're off in time, etc.
- [ ] Export any relevant [records](https://handbook.tts.gsa.gov/records-management/) and store in Google Drive.
- [ ] Clean up infrastructure
  - [ ] [Ask cloud.gov](https://cloud.gov/contact/) for the organization to be deleted.
  - [ ] Delete any associated AWS resources, and decommission any AWS accounts. Ask in [#infrastructure](https://gsa-tts.slack.com/messages/infrastructure) for help.
  - [ ] If the site was operated on Federalist, contact [federalist-support@gsa.gov](mailto:federalist-support@gsa.gov) to deprovision the [custom domain](https://cloud.gov/docs/management/custom-domains/) for the site
- [ ] [Archive the GitHub repositor(ies)](https://help.github.com/articles/archiving-repositories/). Ask in [#admins-github](https://gsa-tts.slack.com/messages/admins-github) if you need help.
- [ ] Domain changes
  - [ ] Clean up any DNS entries that are no longer needed, from [the DNS repository](https://github.com/18F/dns) or elsewhere.
  - [ ] Update DNS entries to point to new urls or [set up redirect(s)](https://github.com/18F/pages-redirects#domain-redirects).
  - [ ] Point to Google Form asking about usage—see [the Fugacious page](https://fugacious.18f.gov/) ([code](https://github.com/18F/fugacious-landing)) as an example.
  - [ ] [Delete the domain registration from DotGov](https://home.dotgov.gov/management/#how-do-i-delete-my-domain)
- [ ] Notify other parts of GSA
  - [ ] Assuming it has an ATO, notify GSA IT that the system no longer exists. Ask in [#infrastructure](https://gsa-tts.slack.com/messages/infrastructure) for help.
  - [ ] Email GSA Privacy Office at [gsa.privacyact@gsa.gov](mailto:gsa.privacyact@gsa.gov) so they can take down the [SORN](https://before-you-ship.18f.gov/privacy/)
  - [ ] Fill out and send the `Disposal Notification Template`, which can be found in the list of [IT Security Forms](https://insite.gsa.gov/portal/content/627238)
- [ ] Clean up external services
  - [ ] Remove (sub)accounts
    - [ ] New Relic - [#admins-newrelic](https://gsa-tts.slack.com/messages/admins-newrelic)
    - [ ] PagerDuty
    - [ ] Twilio
  - [ ] Remove any external integrations
    - [ ] [Slack](https://handbook.tts.gsa.gov/slack/#integrations)
  - [ ] Archive the Slack channel
  - [ ] Archive the issue tracker (Trello, etc.)
