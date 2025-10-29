# Experiment 04: Email Header Analysis & Spoofing Detection

## Objective
To analyze email headers and detect possible spoofing using Mail Header Analyzer (MHA).

## Tools Used
- Mail Header Analyzer (MHA)
- 
- <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/8dc11484-a580-4bea-97d1-791fa1833164" />

- Email Clients (Gmail, Outlook, Yahoo)

- 
- MXToolbox / G Suite Toolbox

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/3cc46f54-ae39-41c6-97a4-0228eb7ae449" />
<img width="1864" height="906" alt="Image" src="https://github.com/user-attachments/assets/8f21c6d3-85a2-4c86-b216-682fbdb269bb" />


## Procedure
1. **Access Header**:
   - Gmail → More (⋮) → Show original

 <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/279b745e-55e9-4b25-b040-1348e6c9df2a" />

-
   - Outlook → File → Properties → Internet headers
   - Yahoo → More (⋮) → View raw message
2. **Copy Header Text** → Extract metadata.

   <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/71741f3b-551d-45d3-a09d-3957f20f9780" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/cd457841-0384-4adb-8875-46e19aceb8ef" />


5. **Analyze Key Fields**:
   - From / To / Return-Path / Message-ID
   - Received (trace server hops)
   - SPF / DKIM / DMARC (authentication)
   - <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/d50e3a6a-1d28-44b1-8969-e0ed1582a2e0" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/6c116385-5188-4dce-9578-3e2ec37fab66" />
6. **Check Received Fields**:
   - Verify hops in reverse order.
   - Detect mismatched IPs/hosts.
  
   -  <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/085d301d-e28a-440b-b5c6-38c81937bbe7" />
   
   - <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/e16914ea-59c2-4a9c-977d-3bc05f03ffc0" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/3258d5f7-dc2f-484e-8587-acf1106d703f" />

  


7. **Authentication Checks**:
   - SPF → Authorized sending server
   - DKIM → Content integrity
   - DMARC → Alignment check
  

8. **Look for Anomalies**:
   - Domain mismatches
   - Suspicious IPs
   - Timestamp gaps
9. **Use Tools**: MXToolbox / G Suite Toolbox for automated analysis.

## Result
- Extracted and analyzed headers with MHA.
- Identified anomalies in SPF/DKIM/DMARC.
- Logged suspicious IPs and mismatched domains.

## Conclusion
Email header analysis is critical for detecting spoofing and phishing by verifying server hops and authentication records.
