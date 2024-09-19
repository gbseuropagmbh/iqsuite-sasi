
![gbs_final_logo-148x58.png](https://gbs.com/wp-content/uploads/2022/04/gbs_final_logo-148x58.png)

# Quick Reference

- Where to get help: [our Support](https://gbs.com/product-support/)

# What is iQ.Suite?

iQ.Suite is an Email Management and Collaboration Security platform that provides enterprise-level security, productivity and compliance for your communication. iQ.Suite covers all relevant aspects of a universal email management solution:

- Malware Protection
- **Spam & Content Recognition**
- Data Loss Prevention
- Encryption
- Disclaimer & Signature Management
- Absence Management
- Connecting Email to Business Plattforms
- Email archiving
- Email Scheduling & Budgeting

# What is SASI Daemon intended for?

SASI (Sophos Anti-Spam Interface) is part of the **iQ.Suite Wall** module which is intended to detect spam messages in emails. The **SASI Daemon** (SASID) can determine the spam probability of messages.

# Was ist iQ.Suite?

iQ.Suite ist eine Plattform für E-Mail-Management und Collaboration Security, die Sicherheit, Produktivität und Compliance für Ihre Kommunikation auf Enterprise-Niveau bietet. iQ.Suite deckt alle relevanten Aspekte einer universellen E-Mail-Management-Lösung ab:

- Malware-Schutz
- **Spamschutz**
- Data Loss Prevention
- Verschlüsselung
- Haftungsausschluss & Signaturmanagement
- Abwesenheitsmanagement
- E-Mail-Archivierung
- Zeitgesteuerter E-Mail-Versand
- E-Mail-Budgetierung

# Wozu dient SASI Daemon?

SASI (Sophos Anti-Spam Interface) ist Teil des Moduls **iQ.Suite Wall**, das zur Erkennung von Spam-Inhalten in E-Mails dient. SASI Daemon (SASID) ermöglicht es, die Spamwahrscheinlichkeit von Nachrichten zu ermitteln.

# Usage

[Helm](https://helm.sh/) must be installed to use the charts. Please refer to Helm's [documentation](https://helm.sh/docs/) to get started.

Once Helm is set up properly, add the repo as follows:
```
helm repo add iqsuite-sasi https://gbseuropagmbh.github.io/iqsuite-sasi/
```

You can then run ```helm search repo iqsuite-sasi``` to see the charts.

# Installing the Chart
 To install the chart with the release name my-release:
 
  ```helm install my-release iqsuite-sasi/sasidaemon ```

# Network policy
The network policy is disabled by default. If you want to enable the network policy, install or update the deployment with ``` --set networkPolicy.enabled=true ```

``` helm install my-release iqsuite-sasi/sasidaemon --version 1.0.1 -n iqsuite-sasi --create-namespace --set networkPolicy.enabled=true ```

# Uninstalling the Chart  
To uninstall/delete the my-release deployment:

 ```helm delete my-release ```
 
 The command removes all the Kubernetes components associated with the chart and deletes the release.
