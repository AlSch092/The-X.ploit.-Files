# The X(ploit)-Files

A detailed list of vulnerabilities found by the author in online games using primarily outbound packet manipulation throughout the past 15 years (only high and critical-ranked severities included). Multiple different file formats will be included such as JSON, HTML, PDF, etc. Best viewed by grabbing the `index.html` and `vulnerabilities.json` files and running `python -m http.server` from the same directory as the two files.

All findings were discovered by the repository owner/document author (alsch092 on GitHub), unless otherwise stated. In rare cases where a finding required the convergence or chaining of separate ideas, one additional contributor may be credited. Not all findings have been added to the documents yet; many more will be added over time as I find time to complete their write-ups - any entries already inclded may also be edited/improved as needed.  

## Introduction: 
This project is intended as a defensive study and reference for secure online-game engineering. It is not intended to serve as an exploit recipe book for modern live games, nor as a smear campaign against any listed game, developer, or publisher.  

The findings documented here focus on historical vulnerability classes in online games, especially issues involving packet handling and serialization logic flaws, client/server trust boundaries, server-side state validation, virtual economy abuse, item/currency generation, replay or impersonation flaws, and scalable automation risks.   
Successful vulnerability discovery via outbound game packets is where creativity crosses with technical prowess, and elegant discoveries/methods can arguably be considered an art form (depending on the level of knowledge or appreciation one has on the subject). Early 2000's-era Games such as MapleStory and Diablo II bred what was possibly the first generation of exceptionally talented and dedicated game hackers, with some spending over a thousand hours on testing and idea brainstorming, with many later becoming AppSec professionals, Software developers, or working as red/blue teamers for gaming companies.  

The direction of game hacking has primarily moved towards commercial FPS and non-exploitative "mass botting" in MMORPGs, as the quality of server code (in particular to this case, packet handling & replication logic) has increased significantly over the past decade, forcing an increased time and effort investment to discover elegant and/or impactful vulnerabilities, in addition to requiring workarounds to increasingly complex anti-cheat solutions (in order to reverse engineer netcode/encryption methods used by games).  

## Inclusion Criteria:

This portfolio only includes historical game-security findings rated High or Critical based on one or more of the following:

- Direct currency, item, or premium-point generation  
- Scalable automation or clientless exploitation  
- Cross-account, actor, or session impersonation  
- Force-control of other players or denial-of-service impacts (including individual players, game channels, or servers)    
- Major virtual economy manipulation   
- Server-side trust-boundary failure   
- Item duplication, rollback abuse, or state desynchronization   
- Exploitability across multiple regions, versions, or game systems
- Serialization logic errors, such as the improper handling of Protobuf fields (bad conditonal logic of payload fields, in cases where context determines which fields are included in the outbound data)  

Lower-impact bugs such as visual-only glitches, minor client-side bypasses, and non-security gameplay bugs are intentionally omitted.  

## Severity Rubric:

**Critical** findings are issues that could directly cause large-scale economy damage, arbitrary currency/item generation, cross-account impact, scalable automation, server trust-boundary compromise, or widespread service disruption.

**High** findings are issues that enabled meaningful unfair advantage, high-value item abuse, significant automation, bypass of intended progression/economy controls, or reliable disruption of other players, but with more limited scale or prerequisites.

## Games with Findings:
- MapleStory (All regions, primarily Global)  
- MapleStory "N" (NA)   
- DragonNest (All regions, primarily SEA and NA)  
- Tree of Savior (All regions, primarily NA)  
- Mir4 (Global)     
- Mir Mobile/MirM (Global)  
- Path of Exile (Global)  
- Honor of Heirs
- ...Potentially more in case I'm not remembering any at the moment  

## End Note:  
If you enjoyed reading the information found in this project or found it helpful as a game developer or game security manager/employee/stakeholder, I'd be happy to chat about potentially helping with improving the security of your online game - either through adversarial simulations/network protocol vulnerability testing, or defensive code development, secure code reviews, etc. Feel free to email me at aschwarz92@outlook.com; I'm also happy to speak to anyone enthusiastic about the topic of online game security (but please note that I cannot help you try to hack whatever game without explicit permission from its owner).    

## Example Output:

<img width="777" height="465" alt="image" src="https://github.com/user-attachments/assets/036e7546-180e-4292-9974-8d146685d555" />

