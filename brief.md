Version: NAFATH-V4
Track: Cybersecurity

## Overview
Digital services are part of our daily lives, and keeping them secure is becoming more important than ever. A national service provider may depend on mobile applications, AI systems, external software libraries, and internet networks to deliver its services. However, a weakness in just one of these areas could put the entire system at risk.

This brief explores six important topics related to software supply chain security, including protecting sensitive information, understanding AI attacks, securing mobile applications, preventing network routing threats, learning from the Log4Shell vulnerability, and tracking software components.

Although these topics may seem different, they are closely connected. Understanding how they affect each other can help cybersecurity professionals identify risks earlier, protect important systems, and respond more effectively when security problems occur.

## Software
Passwords and API keys should not be written directly into application code. The Twelve-Factor App approach recommends keeping settings that change between deployments in environment variables. This makes it easier to use different settings for testing and production without changing the program itself. It also reduces the chance of accidentally sharing sensitive information when a project is uploaded to GitHub. However, environment variables still need protection, since moving secrets out of the code does not automatically make them safe.

Resource: The Twelve-Factor App – Config - https://12factor.net/config

## AI
Evasion and poisoning are two ways attackers can affect machine learning systems, but they happen at different stages. In an evasion attack, someone changes the input to trick a model that has already been trained. Poisoning happens earlier, when harmful or misleading data is introduced during training. For example, a modified message might slip past a spam filter. Knowing the difference helps security teams decide whether to focus on checking training data, testing inputs, or both.

Resource: NIST – Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://www.nist.gov/publications/adversarial-machine-learning-taxonomy-and-terminology-attacks-and-mitigations-0

## Mobile
OWASP MASVS provides security requirements that developers and testers can use when reviewing mobile apps. It covers important areas such as storing data safely, checking user identities, using encryption, and protecting connections to servers. For example, with a banking app, I would want to know whether saved account information is protected and whether the app sends data securely. MASVS explains what needs to be checked, while the OWASP testing guide offers practical ways to test those requirements.

Resource: OWASP – Mobile Application Security Verification Standard - https://mas.owasp.org/MASVS/

## Networking
BGP hijacking happens when a network incorrectly or deliberately announces internet addresses that belong to another network. This can cause traffic to take the wrong path or become unavailable. RPKI helps by letting address holders publish signed Route Origin Authorizations (ROAs), which say which networks may announce their prefixes. Operators can compare incoming routes against this information and reject invalid announcements. However, RPKI checks the route’s origin, not every network along its path.

Resource: IETF – RFC 6811: BGP Prefix Origin Validation - https://www.rfc-editor.org/info/rfc6811/

## Cybersecurity
Log4Shell (CVE-2021-44228) showed how one vulnerable software library can affect many different systems. The problem was found in certain versions of Apache Log4j 2, a tool Java applications use for logging. Under the right conditions, attacker-controlled text could trigger a dangerous JNDI lookup and lead to remote code execution. To respond, organizations needed to find affected Log4j components and update them to supported, fixed versions. Checking dependencies is important because libraries can be included indirectly.

Resource: Apache Logging Services – Security Vulnerabilities - https://logging.apache.org/security.html

## Data
A Software Bill of Materials (SBOM) is a list of the components used to build a software product, including external libraries. It helps security teams find which applications may use a vulnerable component. According to NTIA, the minimum data fields include the supplier, component name and version, other identifiers, dependency relationships, SBOM author, and timestamp. An SBOM does not make software secure on its own, but it makes investigating new vulnerabilities faster and more organized.

Resource: NTIA – The Minimum Elements for a Software Bill of Materials - https://www.ntia.gov/sites/default/files/publications/sbom_minimum_elements_report_0.pdf

## Misconception in My Track

## Open Question
