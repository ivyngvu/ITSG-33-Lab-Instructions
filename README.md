# ITSG-33 Security Assessment Labs

## Overview

Welcome to the **IBM Bob Developer Day - Track D: Secure Development with IBM Bob**!

These hands-on labs teach you how to accelerate Authority to Operate (ATO) readiness and security assessment preparation using IBM Bob as your AI-powered security assessment assistant.

## 🎯 Learning Objectives

By completing these labs, you will:
- ✅ Understand ITSG-33 security controls and their importance for federal systems
- ✅ Learn how to use Bob's custom modes for specialized security assessment
- ✅ Systematically identify security vulnerabilities across 10 critical control families
- ✅ Generate professional security assessment reports
- ✅ Understand remediation priorities and best practices
- ✅ Accelerate ATO readiness from weeks to minutes

## 📋 Prerequisites

### Required Setup
- **Pre-configured VM** with the vulnerable banking application and Bob configuration
- **IBM Bob** installed and configured in VS Code
- **Access to these lab instructions** (online or local)

### Knowledge Prerequisites

**🎉 Great News: NO prior experience required!**

This workshop is designed to be **beginner-friendly** and **accessible to everyone**:

- ✨ **Never written code?** No problem! Bob will guide you through everything
- ✨ **New to security?** Perfect! You'll learn security concepts as you go
- ✨ **First time with Kubernetes?** That's okay! Bob is there to help you.
- ✨ **Curious to know more about IBM Bob?** You're in the right place!

**The Bottom Line:** If you can follow instructions and ask questions, you can complete these labs successfully! Bob does the heavy lifting - you just need curiosity and enthusiasm! 🚀

## 🗂️ Lab Structure

### Lab 0: Introduction to Secure Development with IBM Bob
**Duration:** 15-20 minutes  
**Type:** Conceptual + Setup Verification

**What You'll Learn:**
- The banking application architecture
- ITSG-33 security control framework
- The 10 control families we're focusing on
- How Bob's custom modes work
- Traditional vs. Bob-accelerated assessment process

**What You'll Do:**
- Verify your lab environment
- Understand the intentional vulnerabilities
- Switch to ITSG-33 Security Assessor mode
- Test basic scanning capabilities

📄 **[Start Lab 0: Introduction](LAB-0-INTRODUCTION.md)**

---

### Lab 1: Guided Security Assessment
**Duration:** 30-40 minutes  
**Type:** Hands-on Assessment

**What You'll Learn:**
- How to conduct a comprehensive security assessment with Bob
- Systematic vulnerability detection across all control families
- Evidence collection and documentation
- Report generation for compliance purposes

**What You'll Do:**
- Use Bob to scan the entire application
- Identify intentional vulnerabilities
- Review findings by control family
- Generate a professional assessment report
- Understand remediation priorities

📄 **[Start Lab 1: Guided Assessment](LAB-1-GUIDED-ASSESSMENT.md)**

---

### Lab 2: Advanced Control Analysis (Optional)
**Duration:** 20-30 minutes  
**Type:** Advanced Exploration

**What You'll Learn:**
- Additional ITSG-33 controls beyond the core 10
- Deep-dive analysis of specific control families
- Cross-control dependencies
- Custom security assessment techniques

**What You'll Do:**
- Explore additional control families
- Select controls for deep-dive analysis
- Practice custom security assessments
- Understand control relationships

📄 **[Start Lab 2: Advanced Analysis](LAB-2-ADVANCED-ANALYSIS.md)**

---

## 🏗️ The Vulnerable Banking Application

### What It Is
A realistic banking application with **intentional security vulnerabilities** designed for educational purposes.

### Architecture
- **Frontend:** React + Vite
- **Backend:** Node.js + Express + PostgreSQL
- **Infrastructure:** OpenShift/Kubernetes, Terraform, Ansible

### ⚠️ Important Warning
**DO NOT deploy this application to production!** It contains intentional security vulnerabilities for educational purposes only.

### The Vulnerabilities

The application contains vulnerabilities across 10 ITSG-33 control families:

| Control Family | Vulnerabilities | Severity |
|----------------|-----------------|----------|
| **IA-2:** Identification and Authentication | V-001, V-002 | CRITICAL |
| **IA-5:** Authenticator Management | V-003, V-004, V-005 | CRITICAL |
| **AC-6:** Least Privilege | V-006, V-007, V-008, V-009 | CRITICAL/HIGH/MEDIUM |
| **SC-7:** Boundary Protection | V-010, V-011, V-012, V-013 | CRITICAL/HIGH |
| **SC-28:** Protection of Information at Rest | V-014 | HIGH |
| **CP-9:** Information System Backup | V-015 | CRITICAL |
| **SI-2:** Flaw Remediation | V-016 | HIGH |
| **CM-2:** Baseline Configuration | V-017 | MEDIUM |
| **CA-7:** Continuous Monitoring | V-018, V-019 | MEDIUM/HIGH |
| **SA-12:** Supply Chain Risk Management | V-020 | HIGH |

## 🤖 Bob's Custom Mode System

### ITSG-33 Security Assessor Mode

This custom mode transforms Bob into a professional security assessor with:

**Mode-Specific Rules** (`.bob/rules-itsg33-assessor/`)
- Systematic assessment methodology
- Vulnerability detection patterns

**Reusable Skill** (`.bob/skills/itsg33-vulnerability-detection/`)
- Vulnerability detection patterns (V-001 through V-020)
- Report generation templates
- Control family reference

### How It Works

1. **Switch to ITSG-33 Security Assessor mode** in Bob
2. **Mode-specific rules load automatically** - assessment methodology and patterns
3. **Ask Bob to scan** - it activates the vulnerability detection skill
4. **Bob systematically scans** all application code, infrastructure, and deployment files
5. **Bob identifies vulnerabilities** and maps them to ITSG-33 controls
6. **Bob generates a comprehensive report** with remediation guidance

## 📚 Supporting Materials

### In the Application Repo (Pre-installed on VM)
- **`.bob/custom_modes.yaml`** - Custom mode definition
- **`.bob/rules-itsg33-assessor/`** - Mode-specific assessment rules
- **`.bob/skills/itsg33-vulnerability-detection/`** - Vulnerability detection skill
- **`All_controls.md`** - Complete ITSG-33 control catalog
- **`application/`** - The vulnerable banking application
- **`infrastructure/`** - IaC and deployment configurations

### In This Labs Repo
- **`Subset_Controls.md`** - The 10 focused control families
- **`LAB_UPDATES.md`** - Documentation of recent lab updates

## 🚀 Getting Started

### Quick Start Guide

1. **Verify Your Environment**
   - Ensure you're logged into the pre-configured VM
   - Open Bob with the banking application project
   - Verify Bob is running

2. **Start with Lab 0**
   - Read through the introduction
   - Verify your setup
   - Switch to ITSG-33 Security Assessor mode

3. **Progress Through Labs**
   - Complete Lab 0 (Introduction)
   - Complete Lab 1 (Guided Assessment) - **Core Lab**
   - Optional: Complete Lab 2 (Advanced Analysis)

4. **Expected Time**
   - Lab 0: 15-20 minutes
   - Lab 1: 30-40 minutes
   - Lab 2: 20-30 minutes (optional)
   - **Total: 45-90 minutes**

## 🎓 Learning Path

```
┌─────────────────────────────────────────────────────────────┐
│  Lab 0: Introduction                                         │
│  - Understand the challenge                                  │
│  - Learn about ITSG-33                                       │
│  - Verify your environment                                   │
└────────────────────────┬────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────────────┐
│  Lab 1: Guided Assessment (CORE LAB)                        │
│  - Conduct comprehensive security assessment                 │
│  - Identify vulnerabilities                                 │
│  - Generate professional report                              │
│  - Understand remediation priorities                         │
└────────────────────────┬────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────────────┐
│  Lab 2: Advanced Analysis (OPTIONAL)                        │
│  - Explore additional control families                       │
│  - Deep-dive into specific controls                         │
│  - Practice custom assessments                               │
└─────────────────────────────────────────────────────────────┘
```

## 💡 Tips for Success

### During the Labs
- ✅ **Read carefully** - Each lab builds on previous concepts
- ✅ **Follow step-by-step** - Don't skip verification steps
- ✅ **Ask Bob questions** - Bob is your assistant, use it!
- ✅ **Take notes** - Document interesting findings
- ✅ **Experiment** - Try variations of the commands

### Working with Bob
- 🤖 **Be specific** - Clear questions get better answers
- 🤖 **Use the mode** - Always work in ITSG-33 Security Assessor mode
- 🤖 **Trust the process** - Bob follows a systematic methodology
- 🤖 **Review findings** - Understand why each vulnerability matters
- 🤖 **Learn patterns** - Recognize vulnerability patterns for future use

### Common Issues
- **Bob can't find files?** - Verify you're in the correct project directory
- **Mode not available?** - Check `.bob/custom_modes.yaml` exists
- **No vulnerabilities found?** - Ensure you're in ITSG-33 Security Assessor mode
- **Unexpected results?** - Try restarting Bob or VS Code

## 📞 Support

### During the Workshop
- Raise your hand for instructor assistance
- Check with your neighbors - collaborative learning encouraged!
- Review the troubleshooting sections in each lab

### After the Workshop
- Reference these lab materials
- Review the `.bob/STRUCTURE_CHANGES.md` for configuration details
- Explore the complete ITSG-33 control catalog in `All_controls.md`

## 🎯 Success Criteria

You'll know you've successfully completed the labs when you can:
- ✅ Switch to and use Bob's custom modes
- ✅ Conduct a systematic security assessment
- ✅ Identify vulnerabilities in the banking application
- ✅ Map vulnerabilities to ITSG-33 controls
- ✅ Generate a professional assessment report
- ✅ Understand remediation priorities
- ✅ Explain how Bob accelerates ATO readiness

## 🌟 What's Next?

After completing these labs, you can:
- Apply these techniques to your own projects
- Create custom Bob modes for your specific needs
- Extend the vulnerability detection patterns
- Integrate Bob into your CI/CD pipeline
- Share your knowledge with your team

## 📖 Additional Resources

- **IBM Bob Documentation** - Official Bob documentation
- **ITSG-33 Framework** - Canadian government security controls
- **NIST 800-53** - US equivalent security control framework
- **OWASP Top 10** - Common web application vulnerabilities

---

## 🚀 Ready to Begin?

**Start with [Lab 0: Introduction to Secure Development with IBM Bob](LAB-0-INTRODUCTION.md)**

Good luck, and enjoy learning how to accelerate security assessments with IBM Bob! 🎉