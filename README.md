# **The Bybit Heist**

### **Introduction**
In this GitHub repository, I’ll be sharing details about the **2025 cyber heist** that took place on **February 21st**, grabbing global attention due to the **staggering $1.5 billion** stolen by North Korean hackers.

Since such a **large scale theft** was successfully executed, we can categorize the attackers as either an **organized crime group** or **nation state actors**—after all, this is the **biggest cryptocurrency heist ever recorded!**  

Given the **magnitude** of this attack, cybersecurity professionals and enthusiasts **must** understand exactly how it happened, as well as the possible **defensive strategies, mitigation techniques, and detection methods** to prevent similar incidents in the future.

---

### **Attack Breakdown**

Now, let’s talk about how this whole attack happened. It all started when the attackers used a **social engineering technique** to trick a developer working at Safe{Wallet}. They managed to compromise his workstation, and from there, they stole **AWS session tokens**. These tokens gave them access to Safe{Wallet}'s AWS account, and since they’re temporary credentials, they also allowed the attackers to bypass MFA controls. Smart and sneaky, right?

But they didn’t stop there. Using those stolen tokens, they gained elevated privileges in the AWS system. With this new access, they pulled off something really clever,they manipulated the **user interface (UI)** that Bybit employees interact with. Instead of the regular, harmless JavaScript code, the attackers replaced it with **malicious code**. This code targeted specific Bybit wallets, making sure the stolen ETH (Ethereum) landed in their wallets without raising suspicion.

The timing was everything. These North Korean hackers planned their actions to look like regular work being done during the developer’s normal working hours. Pretty genius for staying undetected, don’t you think? Finally, on **February 21, 2025**, Bybit employees unknowingly signed off on what they thought was a legit transfer, and that’s when the attackers made their move—$1.5 billion was redirected to **wallets controlled by the attackers**.

---

### **Mapping to MITRE ATT&CK**

To understand the technical side of how this attack happened, we can map each phase to the **MITRE ATT&CK framework**. Here’s a quick look at the breakdown:

| **Attack Phase**         | **Action Taken**                          | **MITRE ATT&CK Technique**        | **Technique ID** |
|---------------------------|-------------------------------------------|------------------------------------|------------------|
| Social Engineering        | Developer tricked to compromise workstation | Phishing                          | T1566            |
| Credential Harvesting     | Stealing AWS session tokens              | Valid Accounts                    | T1078            |
| Privilege Escalation      | Gaining elevated AWS access              | Abuse Elevation Control Mechanism | T1548            |
| Defense Evasion           | Timing activity during work hours        | Masquerading                      | T1036            |
| UI Manipulation           | Replacing benign code with malicious code | Content Injection                 | T1659            |
| Exfiltration              | Transferring ETH to controlled wallets   | Exfiltration Over C2 Channel      | T1041            |

By mapping the attack to these techniques, we get a clear picture of how the adversaries worked through the phases of their heist.

---

### **Lessons Learned**

Now, you might be thinking,how could this attack have been stopped? Well, there are a few lessons that stand out here.

1. **Always verify MFA**: The attackers bypassed MFA by using session tokens, so improving token security and monitoring session activity could have made a big difference.
2. **Monitor privileged activities**: Timing their activities to work hours was sneaky, but behavior monitoring tools might have caught the unusual access patterns.
3. **Application security**: Regular security reviews of the UI code could’ve spotted and stopped the malicious injection.

As a cybersecurity professional (or enthusiast), understanding these vulnerabilities and how to address them is essential. This attack shows us how creative and resourceful attackers can be—and why we need to be just as innovative in defending against them.

---

### **Resources**

- [Wilson Center - Bybit Heist Details](https://www.wilsoncenter.org/article/bybit-heist-what-happened-what-now)
- [MITRE ATT&CK Framework](https://attack.mitre.org/)
