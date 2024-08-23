# My First Postmortem

## Issue Summary

- **Duration:** 2 hours (August 22, 2024, 3:00 PM - 5:00 PM UTC)
- **Impact:** The user authentication service was down, preventing users from logging in or accessing their accounts. Approximately 80% of users were affected.
- **Root Cause:** A misconfigured firewall rule blocked access to the authentication service.

## Timeline

- **3:00 PM:** Issue detected through monitoring alerts indicating a significant drop in login traffic.
- **3:05 PM:** Engineers begin investigating the issue, initially suspecting a database failure.
- **3:15 PM:** Database checks confirm it is functioning correctly.
- **3:30 PM:** Focus shifts to the network, and a misconfigured firewall rule is identified.
- **3:45 PM:** Network team is contacted to resolve the issue.
- **4:00 PM:** Firewall rule is corrected.
- **4:10 PM:** User authentication service is restored, and normal login traffic resumes.
- **4:30 PM:** Monitoring confirms the issue is fully resolved.

## Root Cause and Resolution

The root cause was a newly deployed firewall rule that inadvertently blocked all traffic to the user authentication service. The rule was part of a security update but was incorrectly configured. The issue was resolved by reverting the firewall rule to its previous state and implementing a proper configuration after reviewing the security update requirements.

## Corrective and Preventative Measures

- **Improvements Needed:**
  - Enhance firewall rule deployment procedures to include a thorough review process.
  - Implement automated testing for network configuration changes.
  
- **Specific Tasks:**
  - [ ] Review and update the firewall rule deployment checklist.
  - [ ] Develop automated tests for firewall rule changes.
  - [ ] Conduct training for the network team on firewall rule best practices.

# Make People Want to Read Your Postmortem

In the fast-paced tech world, getting people to read a postmortem can be challenging. Here are some tips to make your postmortem more engaging and ensure it catches your audience's attention.

## 1. Start with a Hook

Open with a compelling story or a surprising fact about the outage. For example, "Imagine being locked out of your account on a Friday night—annoying, right? That’s exactly what happened to 80% of our users last week."

## 2. Use Visuals

Add a diagram showing the affected system components and how the issue spread. Visual aids can simplify complex information and make it more digestible.

![Incident Diagram](https://example.com/incident-diagram.png)

## 3. Inject Humor

A little humor can go a long way in keeping readers engaged. Try light-hearted jokes or memes related to the outage.

_"Looks like our firewall rule wanted to play hide and seek with our users!"_

## 4. Be Concise and Clear

Avoid jargon and keep your language simple. Focus on the key points and ensure your postmortem is easy to understand, even for non-technical staff.

## 5. Highlight Key Takeaways

End with a clear summary of what was learned and the actions being taken to prevent future incidents. Use bullet points or a numbered list for clarity.

**Key Takeaways:**

- Improved firewall rule review process.
- Implementation of automated network configuration tests.
- Enhanced team training on security practices.

By making your postmortem informative and engaging, you can ensure it is not only read but also remembered.

