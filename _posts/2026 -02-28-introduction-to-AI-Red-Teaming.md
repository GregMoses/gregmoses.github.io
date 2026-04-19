---
title: "**Introduction to AI Red Teaming**"
author: Gregory Moses
date: 2026-02-28
categories: [Cybersecurity, AI redteaming]
tags: [AI redteam, Prompt injection, Jailbreaks, AI security, OWASPTop10 LLM]
---

AI red teaming is a specialized security practice where I take on the role of a friendly adversary hacker to find weaknesses in artificial intelligence systems. 
While traditional security focuses on bugs in code AI red teaming focuses on the model’s behavior and logic. I intentionally try to trick confuse or manipulate the AI to see if it will leak data provide dangerous information or ignore its safety rules. By finding these flaws before a real attacker does I help make the system safer for everyone.

## Prompt Injection
I test for prompt injection by attempting to override the original instructions of the AI with new malicious ones. This occurs when I provide an input that the model mistakes for a system command rather than user data. In a direct attack I might tell the AI to ignore all previous rules and instead act as a password reset assistant to steal credentials. In an indirect attack I might place hidden text on a website that the AI reads which then triggers the model to silently exfiltrate user data to my external server.

## Jailbreaking
I use jailbreaking to bypass the safety guardrails and ethical filters built into a model. This involves crafting complex scenarios or roleplay environments where the AI feels permitted to generate restricted content. I might use the persona adoption technique where I ask the AI to act as an unfiltered research assistant or use character encoding tricks like Base64 to hide forbidden words from the initial safety scanner. My goal is to find the specific linguistic pressure points that cause the model to ignore its programmed boundaries.

## Data Poisoning
I investigate data poisoning by looking at how a model’s behavior can be corrupted during its training or fine tuning phase. If I can influence the data a model learns from I can create a backdoor that only triggers when a specific keyword is used. This is a long term security risk because the vulnerability is baked into the model's "brain" itself. I simulate this by checking if the model has been trained on public datasets that are easily manipulated or if it learns live from unverified user feedback.

## Insecure Output Handling
I check for insecure output handling by observing what happens when the AI generates code or commands that are automatically executed by another system. If the AI is tricked into writing a malicious script and the hosting application runs that script without checking it first I have successfully performed an exploit. This vulnerability is dangerous because it turns a simple text generation tool into a functional weapon that can delete databases or install malware on a user's machine.

## Training Data Extraction
I perform training data extraction attacks to see if the model will accidentally reveal sensitive information it learned during its creation. By using specific repetitive prompts or "membership inference" techniques I try to get the AI to spit out addresses private names or proprietary code snippets that should have been kept secret. This test is vital for privacy compliance as it ensures that the AI hasn't memorized private records that it might later repeat to a random user.

## Denial of Wallet
I test for denial of wallet vulnerabilities which target the financial cost of running large AI models. By sending extremely long complex or recursive queries I attempt to maximize the computational power and "tokens" used by the system. If I can automate this I can quickly drain the owner's API budget or slow down the service for legitimate users. This is the AI version of a traditional denial of service attack focusing on resource exhaustion and financial impact rather than just crashing a server.
