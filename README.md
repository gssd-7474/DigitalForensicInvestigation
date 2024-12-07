# Digital Forensics Investigation: Alex Marshall Case

## Overview
This project is a comprehensive **Digital Forensics Investigation** into the suspicious death of Alex Marshall. The investigation examines multiple pieces of evidence, including disk images, memory dumps, network captures, and a damaged mobile phone, using advanced forensic tools and techniques. The goal is to uncover critical clues, reconstruct the timeline, and identify the individuals involved in the case.

---

## Evidence Analysis

### Evidence A: Disk Image of Alex's Desktop Computer
1. **Description**: 
   - Contains 11 disk files combined into a single `.dd` file for analysis.
   - Revealed critical information about Alex's financial struggles, academic stress, and emotional state.

2. **Key Findings**:
   - **Registry Analysis**: Identified Alex as the laptop owner.
   - **Programs**: Recent applications include Firefox and MS Paint.
   - **Recovered Files**:
     - `UniversityWarning_Letter.pdf`: Academic probation notice.
     - `notes.jpg`: Alex’s will, indicating regret and leaving possessions to his family.
   - **State of Mind**: Evidence of financial debt, family pressure, and academic struggles contributing to stress.

---

### Evidence B: Dormitory Network Capture
1. **Description**:
   - A `.pcap` file analyzed using Wireshark and NetworkMiner.

2. **Key Findings**:
   - **Participants**: Conversations between Alex (AlexM21) and individuals such as DormKing, PartyDude, LilyLaw, and ArtLover99.
   - **Files Transferred**: SSL key and `ExamSample.png` containing exam questions.
   - **Timeline**: Communications between 07:57 and 08:46 UTC on Sep 1, 2024.
   - **Context**: Revealed relationship conflicts and academic cheating schemes.

---

### Evidence C: Memory Dump from Sophia’s Laptop
1. **Description**:
   - RAM dump analyzed using Volatility.

2. **Key Findings**:
   - **Applications**: Running processes included Firefox, Thunderbird, and custom applications.
   - **Emails**: Emotional correspondence between Sophia and Alex, indicating a close relationship.
   - **Web Searches**: Topics like "how to stop someone from leaving you" and "self-defense" suggest emotional distress.
   - **Password**: The system password was found to be “Alexisbeautiful,” hinting at Sophia’s attachment to Alex.

---

### Evidence D: Damaged Mobile Phone Disk Image
1. **Description**:
   - Mounted disk image from a damaged phone found in Alex’s apartment.

2. **Key Findings**:
   - **Contacts**: Four key contacts and three suspiciously deleted numbers.
   - **Messages and Calls**:
     - Conversations with Lily Parker, Sophia Bennett, and an unknown contact.
     - Threatening messages related to unpaid debts.
   - **Web Searches**: "Emergency loans" and "nearest campus security" reflect fear and desperation.
   - **Encrypted File**: Found `recording.aes`, potentially hiding critical information.

---

## Timeline Reconstruction
Timelines were created for each piece of evidence using tools like `mactime` and Volatility's `timeliner`. The consolidated timeline revealed:
1. Alex’s escalating financial and emotional struggles.
2. Network communications on Sep 1, 2024, showing manipulation and threats.
3. Interactions between Sophia and Alex before the incident.

---

## Tools Used
- **Volatility**: For memory analysis.
- **Wireshark & NetworkMiner**: For network packet analysis.
- **FTK Imager**: For creating forensic images.
- **RegRipper**: For extracting registry data.
- **Sleuth Kit**: For timeline creation and file analysis.

---

## Task 2: Memory Forensics Analysis
This section focuses on **Memory Forensics**, a critical area of digital forensics used to analyze volatile memory (RAM). This analysis played a pivotal role in understanding the case, particularly with evidence from Sophia's laptop.

### Key Findings:
1. **Applications**: Identified running processes such as Firefox and Thunderbird.
2. **Email Analysis**: Recovered emotional emails between Sophia and Alex, indicating a close relationship.
3. **Web Searches**: Topics like "how to stop someone from leaving you" and "signs of cheating" suggested insecurity and potential motives.
4. **Password Discovery**: Sophia's laptop password, “Alexisbeautiful,” pointed to a strong emotional attachment.

### Tools and Techniques:
- **Volatility**:
  - `pstree`: Listed all running processes.
  - `imageinfo`: Identified the system profile.
  - `lsadump`: Extracted sensitive authentication details.
- **Challenges**:
  - Volatile nature of RAM made precise timing crucial.
  - Large memory dump size required significant computational resources.

### Recommendations:
- Use **write blockers** during acquisition to ensure data integrity.
- Leverage tools like **Volatility** for advanced memory analysis.
- Establish robust chain-of-custody protocols to ensure evidence legitimacy.

---

## Conclusion
The investigation unveiled a complex web of relationships, financial struggles, and emotional distress contributing to Alex’s tragic death. The memory forensics analysis in Task 2 highlighted critical details, reinforcing the importance of volatile memory in forensic investigations. Each piece of evidence played a crucial role in reconstructing events, showcasing the power of digital forensics in solving complex cases.

**Disclaimer**: This project is intended for educational purposes and showcases the process of conducting a professional digital forensic investigation.
