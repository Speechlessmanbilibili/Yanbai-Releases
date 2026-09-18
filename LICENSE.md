# Yanbai End User License Agreement

**English** | [简体中文](LICENSE_zh.md)

Version 1.5 · Effective 12 September 2026

Copyright © 2026 SilentPerson. All rights reserved.

PLEASE READ THIS AGREEMENT CAREFULLY. This End User License Agreement (the “Agreement”) is a legal agreement between you (“you”, the “Licensee”) and the copyright holder of the software known as Yanbai (砚白) (the “Licensor”), and it governs your use of that software. By downloading, installing, copying, or otherwise using the software, you confirm that you have read, understood, and agree to be bound by this Agreement. If you do not agree to any part of this Agreement, you must not download, install, or use the software.

## 1. Definitions

1.1 “Software” means the computer program known as Yanbai (砚白) in object code form, together with the installers, archives, documentation, and any updates or supplements distributed by the Licensor, but excluding the Third-Party Components defined in Section 1.6.

1.2 “Official Distribution Channel” means the repository published by the Licensor at <https://github.com/Speechlessmanbilibili/Yanbai-Releases>, including its release pages and its issue tracker.

1.3 “you” and “Licensee” mean the individual person, or the legal entity, that downloads, installs, or uses the Software. Where a legal entity is the Licensee, “you” also includes (a) that entity's affiliates, and (b) the employees and contractors of that entity and of its affiliates, in each case only when they act on the entity's behalf. Where you use the Software on behalf of a legal entity, you represent that you are authorized to bind that entity to this Agreement.

1.4 “Commercial Use” means any use of the Software by a commercial entity, or any use for or on behalf of a commercial entity, or in the course of a trade, business, or profession, whether or not for direct monetary compensation.

1.5 “Internal Deployment” means reproduction and distribution of the Software within your organization, that is, between you and your affiliates and to your employees and contractors, for internal business purposes, provided that the Software is not made available to the public and no fee is charged for it.

1.6 “Third-Party Components” means the software libraries, runtimes, and fonts, in source or binary form, that are incorporated in or distributed with the Software and that are owned by parties other than the Licensor. A list is provided in the file `THIRD_PARTY_NOTICES.md` distributed with the Software.

1.7 “Notice” means a written communication sent through the channel designated in Section 14.

1.8 “your organization” means you and, where you are a legal entity, your affiliates, together with the employees and contractors of each of them.

## 2. Grant of License

2.1 Subject to your compliance with this Agreement, the Licensor grants you a limited, non-exclusive, non-transferable, non-sublicensable, royalty-free license, terminable only as provided in Section 2.3, to:

(a) download and install copies of the Software obtained from the Official Distribution Channel;

(b) use the Software for personal purposes and for Commercial Use, without limitation as to the number of documents, the number of users, or duration;

(c) reproduce a reasonable number of copies of the Software for backup and archival purposes, including copies held by colleagues within your organization as part of Internal Deployment; and

(d) carry out Internal Deployment.

2.2 All rights not expressly granted in this Agreement are reserved by the Licensor.

2.3 The license granted in this Section 2 remains in effect for as long as you comply with this Agreement. The Licensor may terminate it only on the grounds set out in Section 10.2, and, except where the breach is incapable of remedy (for example, unauthorized redistribution of the Software) or where continued use would cause irreparable harm, the Licensor will first give you Notice and a reasonable period of at least thirty (30) days to remedy the breach. No refund is due on termination, as no fee was paid.

## 3. Restrictions

3.1 You shall not, and shall not permit any third party to:

(a) distribute, sublicense, sell, resell, rent, lease, lend, or otherwise make the Software available to any person or entity outside your organization; Internal Deployment within your organization is permitted under Section 2.1(d);

(b) incorporate the Software into another product, installation medium, or software repository for distribution outside your organization, or distribute it as part of such a bundle, without the prior written consent of the Licensor. This does not restrict internal software sources, system images, or device-management distribution within your organization as permitted by Section 2.1(d);

(c) reverse engineer, decompile, or disassemble the Software, except to the extent that such a restriction is expressly prohibited by applicable law;

(d) remove, obscure, or alter any copyright notice, attribution, or license text contained in or displayed by the Software, including the files `LICENSE.md`, `LICENSE_zh.md`, and `THIRD_PARTY_NOTICES.md` distributed with it;

(e) use the names “Yanbai” or “砚白”, or the name of the Licensor, to promote a modified or derivative build in a manner that suggests that the build originates from, or is endorsed by, the Licensor; or

(f) use the Software for any purpose that is unlawful under applicable law.

3.2 Package managers, public software repositories, and other distributors that wish to carry the official artifacts must obtain the prior written consent of the Licensor. Such consent may be requested through the channel in Section 14.

3.3 No patent license, trademark license, or other intellectual property license is granted under this Agreement except as expressly stated. All product names, trade names, and trademarks remain the property of their respective owners.

## 4. Third-Party Components

4.1 The Software incorporates Third-Party Components, including components of the Rust ecosystem, Tauri, KaTeX, Mermaid, and the HarmonyOS Sans SC font. The complete list, with versions and licenses, is the file `THIRD_PARTY_NOTICES.md` distributed with the Software.

4.2 Third-Party Components are governed exclusively by their own license terms. This Agreement does not modify, restrict, or supersede those terms, and it grants no rights in respect of Third-Party Components beyond those conferred by their own licenses. Where a Third-Party Component is offered under more than one license, the Licensor relies on the option recorded in the “Selected” column of `THIRD_PARTY_NOTICES.md`.

4.3 Within the scope of your use of the Software under this Agreement, you are responsible for complying with those terms. The license texts of the bundled fonts are distributed in the directory `THIRD_PARTY_LICENSES/`.

## 5. Source Code

5.1 The Software is distributed solely in object code form. The source code of the Software is not published by the Licensor, and this Agreement grants no right of access to the source code and no right to use or modify it.

5.2 Nothing in this Agreement shall be construed as an open source license. This Section does not restrict any right you may have under the license of a Third-Party Component.

## 6. Data, Privacy, and Updates

6.1 The Software does not collect telemetry, usage statistics, or crash reports, and does not transmit your documents or any part of their content to the Licensor or to any third party.

6.2 The Software does not perform network requests on its own initiative. Its font, mathematics, and diagram resources are bundled and loaded locally.

6.3 Any log files the Software writes are stored locally on your device and are not uploaded.

6.4 The Software does not install updates automatically; new versions are obtained by you from the Official Distribution Channel. Section 9 applies to such releases.

6.5 This Section describes the Software itself. The operating system, the WebView runtime, and other software on your device may perform their own network activity, which is outside the Licensor's control.

6.6 The Software keeps an encrypted crash-recovery draft of open documents in a file named `recovery.enc` inside its application data directory. That file stores the full text of the documents you have open, together with the file paths involved, in encrypted form using AES-256-GCM, with the encryption key protected by the current operating system user's login credentials (using Windows DPAPI on Windows, and strict user-level permission isolation on Unix-like systems). It cannot be decrypted outside the current user's login session. It is written while you edit and is cleared when you close the documents normally. Delete the file if you do not want the draft to remain.

6.7 If a future version changes how data is handled, the Licensor will state the change in that version's release notes.

## 7. Your Content

7.1 You retain all rights, title, and interest in the documents you create, open, edit, save, paste into, or export with the Software. The Licensor claims no ownership of, and no license to, that content.

7.2 The Software processes your documents locally on your device. You are responsible for maintaining backups of documents you consider important.

## 8. Feedback

8.1 If you submit feedback, suggestions, or defect reports, you grant the Licensor a perpetual, worldwide, royalty-free, irrevocable license to use and incorporate them into the Software, without any obligation of confidentiality, attribution, or compensation. Feedback is not treated as confidential: do not include confidential information, personal data, or document content in a report. You are not required to submit feedback.

## 9. Updates and Support

9.1 The Licensor may, but is not obliged to, release updates, upgrades, or new versions of the Software. Any such release is governed by this Agreement unless it is accompanied by a separate license agreement.

9.2 The Licensor provides no warranty and assumes no support obligation under this Agreement, whether through an issue tracker, by electronic mail, or otherwise.

## 10. Term and Termination

10.1 This Agreement takes effect upon your first download, installation, or use of the Software and continues until terminated.

10.2 Your rights under this Agreement terminate if you materially breach any provision of this Agreement, the Licensor has given you Notice of the breach under Section 2.3, and you have failed to remedy it within the period stated in that Notice. Upon termination you must cease all use of the Software and delete or destroy all copies in your possession or control.

10.3 The Licensor may revise this Agreement for future releases. A release already distributed remains governed by the version of this Agreement that accompanied it.

10.4 Sections 1, 3, 4, 5, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, and 17 survive termination of this Agreement.

## 11. Disclaimer of Warranty

11.1 THE SOFTWARE IS PROVIDED “AS IS” AND “AS AVAILABLE”, WITHOUT WARRANTY OF ANY KIND, WHETHER EXPRESS, IMPLIED, STATUTORY, OR OTHERWISE, INCLUDING WITHOUT LIMITATION ANY WARRANTY OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, OR NON-INFRINGEMENT.

11.2 WITHOUT LIMITING SECTION 11.1, THE LICENSOR DOES NOT WARRANT THAT THE SOFTWARE WILL BE ERROR-FREE OR OPERATE WITHOUT INTERRUPTION, OR THAT IT WILL PRESERVE OR CORRECTLY PROCESS ANY DOCUMENT.

11.3 No advice or information, whether oral or written, obtained from the Licensor shall create any warranty not expressly stated in this Agreement.

11.4 Some jurisdictions do not allow the exclusion of certain warranties. To the extent such a rule applies to you, the exclusions in this Section apply to the maximum extent permitted by applicable law.

## 12. Limitation of Liability

12.1 TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, THE LICENSOR SHALL NOT BE LIABLE FOR ANY INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, PUNITIVE, OR CONSEQUENTIAL DAMAGES, OR FOR ANY LOSS OF DATA, CORRUPTION OF DOCUMENTS, LOSS OF PROFITS, LOSS OF GOODWILL, OR BUSINESS INTERRUPTION, HOWEVER CAUSED AND UNDER ANY THEORY OF LIABILITY, ARISING OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THIS AGREEMENT, EVEN IF THE LICENSOR HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

12.2 TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, THE AGGREGATE LIABILITY OF THE LICENSOR UNDER OR IN CONNECTION WITH THIS AGREEMENT SHALL NOT EXCEED THE AMOUNT ACTUALLY PAID BY YOU TO THE LICENSOR FOR THE SOFTWARE, WHICH IS ZERO.

12.3 Nothing in this Agreement excludes or limits the Licensor's liability for: (a) death or personal injury caused by the Licensor's negligence; (b) fraud or fraudulent misrepresentation; (c) willful misconduct or gross negligence; or (d) any other liability that cannot be excluded or limited under applicable law.

12.4 If you are a consumer, you may have statutory rights that cannot be waived by contract. Nothing in this Agreement affects those rights.

## 13. Export Control and Sanctions

13.1 You shall comply with all applicable export control and economic sanctions laws and regulations, and shall not export, re-export, transfer, or use the Software in violation of them, including by providing it to any person or entity on a restricted-party list, or for any restricted end use such as the development or production of weapons of mass destruction.

13.2 The Software implements the SHA-256 digest algorithm for file fingerprinting, uses standard AES-256-GCM encryption combined with operating system user credential protection for local recovery draft protection, and does not encrypt communications. You are responsible for determining whether your use requires an export authorization or classification in your jurisdiction.

## 14. Notices

14.1 Notices to the Licensor must be sent by electronic mail to <speechlessmans@outlook.com>. Matters that are not confidential, such as a general question or a permission inquiry, may also be raised through the issue tracker of the Official Distribution Channel at <https://github.com/Speechlessmanbilibili/Yanbai-Releases/issues>. Notices of breach, requests for the written consent required by this Agreement, and anything containing confidential information must be sent by electronic mail. The Licensor will not disclose the contents of an electronic mail notice without your agreement.

14.2 Notices to you may be given by publishing a revised version of this Agreement or a notice on the Official Distribution Channel. Such notice takes effect on publication.

## 15. Assignment

15.1 You may not assign or transfer this Agreement, or any rights under it, without the prior written consent of the Licensor.

15.2 The Licensor may assign this Agreement to an affiliate, or to a successor in connection with a merger, acquisition, or sale of substantially all of its assets, provided that the assignee assumes the Licensor's obligations under Section 6. The Licensor will give Notice of such an assignment.

## 16. Miscellaneous

16.1 This Agreement constitutes the entire agreement between you and the Licensor with respect to the Software and supersedes all prior or contemporaneous understandings regarding its subject matter.

16.2 If any provision of this Agreement is held to be invalid or unenforceable, that provision shall be severed and the remaining provisions shall remain in full force and effect.

16.3 No failure or delay by the Licensor in exercising any right under this Agreement constitutes a waiver of that right.

16.4 This Agreement is executed in the English and Chinese languages. Both texts are equally authentic; in the event of any discrepancy, the English text prevails. Where mandatory law applicable to you requires that the local-language text govern, that requirement prevails over this Section 16.4.

## 17. Governing Law and Dispute Resolution

17.1 This Agreement is governed by the laws of the mainland of the People's Republic of China, without regard to its conflict-of-law rules.

17.2 The Licensor's domicile is in the mainland of the People's Republic of China; it may be confirmed through the channel in Section 14. Any dispute arising out of or in connection with this Agreement shall be submitted to the competent people's court at the Licensor's domicile. If the Licensor assigns this Agreement under Section 15.2, the assignee's domicile replaces the Licensor's for the purposes of this Section.

17.3 If you are a consumer, you may also bring proceedings before the courts of your place of residence where mandatory law so provides.
