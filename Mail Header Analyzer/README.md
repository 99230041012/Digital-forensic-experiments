# Experiment 04: Email Header Analysis & Spoofing Detection

## Objective
To analyze email headers and detect possible spoofing using Mail Header Analyzer (MHA).

## Tools Used
- Mail Header Analyzer (MHA)
- Email Clients (Gmail, Outlook, Yahoo)
- MXToolbox / G Suite Toolbox


## Procedure
1. **Access Header**:
   - Gmail → More (⋮) → Show original
   - Outlook → File → Properties → Internet headers
   - Yahoo → More (⋮) → View raw message
2. **Copy Header Text** → Extract metadata.
3. **Analyze Key Fields**:
   - From / To / Return-Path / Message-ID
   - Received (trace server hops)
   - SPF / DKIM / DMARC (authentication)
4. **Check Received Fields**:
   - Verify hops in reverse order.
   - Detect mismatched IPs/hosts.
5. **Authentication Checks**:
   - SPF → Authorized sending server
   - DKIM → Content integrity
   - DMARC → Alignment check
6. **Look for Anomalies**:
   - Domain mismatches
   - Suspicious IPs
   - Timestamp gaps
7. **Use Tools**: MXToolbox / G Suite Toolbox for automated analysis.

---

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/7b580c7f-d097-4bb5-ae25-f58e101fe60c" />
## Result
- Extracted and analyzed headers with MHA.
- Identified anomalies in SPF/DKIM/DMARC.
- Logged suspicious IPs and mismatched domains.

## Conclusion
Email header analysis is critical for detecting spoofing and phishing by verifying server hops and authentication records.
