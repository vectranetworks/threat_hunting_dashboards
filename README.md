Threat Hunting Dashboards
=========================

# About #
The threat hunting dashboards were created by Sidekick Analysts as part of a series on threat hunting with Recall. The current dashboarrds assist with hunting for DCSync and DCShadow as well as PsExec threats.
Learn more about threat hunting for DCSync, DCShadow, and PSExec from [this](https://event.on24.com/wcc/r/3758948/F4E8BA721E4BB7E14B2326E762AA9031?partnerref=github) webinar

## DCSync and DCShadow ##
Dashboard to assist with hosts potentially performing DCSync or DCShadow techniques.
The source hosts in the bar charts should only be Domain Controllers. Clicking on a bar in the chart will filter in a specific source host; the filter can be negated. Recommend modifying the search to exclude domain controllers by name and saving.

## PsExec ##
This dashboard can help uncover the usage of PsExec in the network from admins, red teams, and threat actors.
Recommend modifying the search to exclude hosts that are known authorized sources by name and saving.
Clicking the _Filter for value_ button in the chart can be helpful for isolating records that are related to suspicious activity.

# Installation #
1. Clone the repo or copy the .json file to your local machine.
2. Import dashboard from JSON - see [elastic reference](https://www.elastic.co/guide/en/kibana/current/saved-objects-api-import.html)
3. Open the dashboard and select the _Edit_ tab from the top menu bar.
4. Add your known Domain Controllers and trusted PsExec administrators to the respective searches.
5. Adjust the time to your desired default value (current time is **Last 7 Days**).
6. Click _Save_, which is again located on the top menu bar, to save your dashboard.
Remember to investigate suspicious activity now, so that you can hunt for and detect threats in the future.

# Reference #
* [Introduction to Threat Hunting with Network Metadata](https://event.on24.com/wcc/r/3758948/F4E8BA721E4BB7E14B2326E762AA9031?partnerref=github)
* [T1003.006](https://attack.mitre.org/techniques/T1003/006/) OS Credential Dumping: DCSync
* [T1207](https://attack.mitre.org/techniques/T1207/) Rogue Domain Controller
* [T1136.002](https://attack.mitre.org/techniques/T1136/002/) Create Account: Domain Account
* [T1543.003](https://attack.mitre.org/techniques/T1543/003/) Create or Modify System Process: Windows Service
* [T1570](https://attack.mitre.org/techniques/T1570/) Lateral Tool Transfer
* [T1021.002](https://attack.mitre.org/techniques/T1021/002/) Remote Services: SMB/Windows Admin Shares
* [T1569.002](https://attack.mitre.org/techniques/T1569/002/) System Services: Service Execution
* [Recall Host Dashboard](https://support.vectra.ai/s/article/KB-VS-1248)