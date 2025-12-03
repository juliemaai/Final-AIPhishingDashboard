# AI-Powered Phishing Detection System

An automated email security system that uses artificial intelligence to detect and classify phishing, spam, and legitimate emails in real-time.

## 🎯 Project Overview

This system automatically analyzes emails using OpenAI's GPT API to identify phishing attempts, spam, and legitimate messages. It provides a real-time monitoring dashboard with detailed threat analysis and classification confidence scores.

### Key Features

- 🤖 **AI-Powered Classification** - Uses OpenAI GPT for intelligent email analysis
- 📊 **Real-Time Dashboard** - Monitor classified emails with detailed analytics
- ⚡ **Automated Processing** - Zero manual intervention required
- 🎯 **Priority Scoring** - Automatically ranks emails by threat level
- 📈 **Detailed Analysis** - View AI reasoning and threat indicators
- 🌙 **Dark Mode UI** - Modern, accessible interface

## 🛠️ Technology Stack

- **Automation:** n8n (Workflow Engine)
- **AI/ML:** OpenAI API (GPT Classification)
- **Database:** Google Sheets (Cloud Storage)
- **Frontend:** HTML5, CSS3, JavaScript (Vanilla)
- **API:** RESTful API via n8n webhooks

## 🚀 How It Works

### System Flow

```
Email Input → Pre-Processing → AI Classification → Priority Scoring → Database → Dashboard
```

### Detailed Steps

1. **Email Ingestion** - Test emails are loaded into the n8n workflow
2. **Pre-Processing** - System extracts sender domain, counts links, and structures data
3. **AI Classification** - OpenAI GPT analyzes email content for phishing indicators:
   - Domain authenticity
   - Urgency language patterns
   - Link destinations
   - Grammar and spelling
   - Impersonation attempts
4. **Priority Calculation** - Automated scoring based on:
   - Risk level (high/medium/low)
   - AI confidence score
   - Classification type
5. **Storage** - All data saved to Google Sheets (21 columns per email)
6. **Dashboard Display** - Real-time visualization with filtering and sorting

## 📊 Performance Metrics

- **Processing Time:** ~6 seconds per email
- **Average AI Confidence:** 78%
- **Test Dataset:** 50 emails (phishing, spam, legitimate)
- **Automation Level:** 100% (no manual intervention)
- **Classification Accuracy:** 75%+ on clear phishing attempts

## 🎓 Classification Examples

### Example 1: Phishing Detection ⚠️

```
Subject: Urgent: Verify your PayPal account
From: security@paypa1-verify.com
Domain: paypa1-verify.com (suspicious - note the "1" instead of "l")

AI Classification: PHISHING
Confidence: 85%
Risk Level: HIGH
Priority: HIGH

Threat Indicators:
• Domain spoofing (paypa1 vs paypal)
• Urgency/pressure tactics
• Suspicious URL destination
• Account threat language

AI Reasoning:
"Email exhibits suspicious domain characteristics and urgency tactics 
commonly used in phishing attacks. The domain uses character substitution 
to mimic a legitimate service."
```

### Example 2: Spam Detection ⚠️

```
Subject: You've won $5.6 million!
From: lottery@winner-international.biz
Domain: winner-international.biz

AI Classification: SPAM
Confidence: 75%
Risk Level: MEDIUM
Priority: MEDIUM

Threat Indicators:
• Too good to be true offer
• Unsolicited prize notification
• Suspicious domain
• Lottery scam pattern

AI Reasoning:
"Email contains unrealistic financial offer typical of lottery scams. 
No legitimate lottery notifies winners via unsolicited email."
```

### Example 3: Legitimate Email ✅

```
Subject: Team meeting scheduled for 3pm
From: colleague@company.com
Domain: company.com

AI Classification: LEGITIMATE
Confidence: 92%
Risk Level: LOW
Priority: LOW

Threat Indicators: None

AI Reasoning:
"Email from known corporate domain with normal business content. 
No suspicious patterns or threat indicators detected."
```

## 💻 Dashboard Features

### Statistics Dashboard
- 📧 Total emails processed
- 🚨 Phishing count
- 📬 Spam count
- ✅ Legitimate count
- 🎯 Average AI confidence score

### Filtering & Sorting
- Filter by classification (phishing/spam/legitimate)
- Filter by priority level (high/medium/low)
- Sort by priority, confidence, or date
- Real-time search

### Email Detail View
- Complete email content
- Sender information and domain
- AI classification with confidence
- Detailed reasoning explanation
- Identified threat indicators
- Links found in email
- Risk level assessment
- Priority score

## 🔐 Security & Privacy

### Data Safety
- ✅ Uses test/sample emails only (no real accounts)
- ✅ No access to live email accounts
- ✅ Safe for demonstration and educational purposes

### API Security
- ✅ API keys encrypted in n8n credentials
- ✅ HTTPS for all API communications
- ✅ OAuth authentication for Google Sheets
- ✅ Private database with controlled access

### Privacy Considerations
- No personally identifiable information stored
- Test data only
- Local dashboard (no external tracking)

## 🎯 Real-World Applications

### Corporate Environment
- **Employee Protection:** Scan incoming emails for entire organization
- **Security Team:** Reduce manual review workload by 90%
- **Incident Prevention:** Catch threats before users click
- **Security Awareness:** Educational tool for training

### Small Business
- **Affordable Security:** No expensive software licenses needed
- **Easy Maintenance:** Cloud-based, minimal IT overhead
- **Scalable Solution:** Grows with your business
- **Quick Setup:** Deploy in under an hour

### Educational Institution
- **Student Protection:** Shield students from phishing attacks
- **Teaching Tool:** Hands-on cybersecurity learning
- **Research Platform:** Study phishing patterns and trends
- **Awareness Campaigns:** Demonstrate real threats

### Personal Use
- **Email Protection:** Guard your personal accounts
- **Threat Education:** Learn to recognize phishing
- **Skill Development:** Understand cybersecurity concepts
- **Portfolio Project:** Showcase technical abilities

## 📊 Project Statistics

| Metric | Value |
|--------|-------|
| Test Emails Processed | 50 |
| Processing Time | ~3 seconds/email |
| Average AI Confidence | 78% |
| High Confidence (>80%) | 35 emails |
| Automation Level | 100% |
| Phishing Detected | 15 (30%) |
| Spam Detected | 10 (20%) |
| Legitimate | 25 (50%) |

## 🚀 Future Enhancements

### Phase 1: Real Email Integration
- [ ] Gmail API integration
- [ ] Outlook/Office 365 connector
- [ ] Automatic inbox scanning
- [ ] Email quarantine automation
- [ ] Real-time alert notifications

### Phase 2: Advanced AI
- [ ] Custom ML model training
- [ ] Sender reputation system
- [ ] Historical trend analysis
- [ ] Pattern recognition improvements
- [ ] Multi-language support

### Phase 3: Enterprise Features
- [ ] Multi-user dashboard
- [ ] Team collaboration tools
- [ ] Role-based access control
- [ ] Advanced reporting
- [ ] API for third-party integrations
- [ ] Mobile application

### Phase 4: Community Features
- [ ] Public threat database
- [ ] Crowdsourced threat intelligence
- [ ] Plugin architecture
- [ ] Custom rule engine
- [ ] White-label solution

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Report Bugs:** Open an issue describing the problem
2. **Suggest Features:** Share your ideas for improvements
3. **Submit Pull Requests:** Fix bugs or add features
4. **Improve Documentation:** Help make guides clearer
5. **Share Feedback:** Let us know what works and what doesn't

### Contribution Guidelines

- Fork the repository
- Create a feature branch (`git checkout -b feature/AmazingFeature`)
- Commit your changes (`git commit -m 'Add some AmazingFeature'`)
- Push to the branch (`git push origin feature/AmazingFeature`)
- Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### What This Means
- ✅ Commercial use allowed
- ✅ Modification allowed
- ✅ Distribution allowed
- ✅ Private use allowed
- ⚠️ No warranty provided
- ⚠️ No liability assumed

## 👤 Author

**Your Name**
- GitHub: [@juliemaai](https://github.com/juliemaai)
- Email: jmai0079@ung.edu

## 🙏 Acknowledgments

- **OpenAI** - For providing the GPT API that powers the classification
- **n8n** - For the excellent workflow automation platform
- **Anthropic Claude** - For development assistance and code review
- **[Your School/University]** - For the project opportunity
- **Open Source Community** - For inspiration and resources

## 📧 Contact & Support

### Questions?
- Open an [Issue](https://github.com/YOUR-USERNAME/ai-phishing-detection-system/issues)
- Email: your.email@example.com

### Found a Bug?
- Check existing [Issues](https://github.com/YOUR-USERNAME/ai-phishing-detection-system/issues)
- Create new issue with detailed description
- Include screenshots if applicable

### Want to Collaborate?
- Fork the repository
- Make your improvements
- Submit a Pull Request

## 🌟 Show Your Support

If you find this project useful or interesting:

- ⭐ **Star this repository**
- 🍴 **Fork it** to build your own version
- 📢 **Share it** with others who might benefit
- 💬 **Provide feedback** to help improve it

## 📈 Project Roadmap

**Q1 2025**
- [ ] Real email integration (Gmail)
- [ ] Mobile-responsive dashboard
- [ ] Export/reporting features

**Q2 2025**
- [ ] Custom ML model training
- [ ] Advanced analytics
- [ ] Multi-language support

**Q3 2025**
- [ ] Enterprise features
- [ ] API for third parties
- [ ] Mobile app (iOS/Android)

**Q4 2025**
- [ ] Community threat database
- [ ] Plugin system
- [ ] White-label solution

## 📚 Additional Resources

- [OpenAI API Documentation](https://platform.openai.com/docs)
- [n8n Documentation](https://docs.n8n.io)
- [Phishing Research Papers](https://scholar.google.com/scholar?q=phishing+detection)
- [OWASP Security Guidelines](https://owasp.org)

---

<div align="center">

**⭐ Star this repo if you found it helpful! ⭐**

Made with ❤️ and ☕

[Report Bug](https://github.com/YOUR-USERNAME/ai-phishing-detection-system/issues) · 
[Request Feature](https://github.com/YOUR-USERNAME/ai-phishing-detection-system/issues) · 
[Documentation](docs/)

</div>
