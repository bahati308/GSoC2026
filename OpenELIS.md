# Security Audit and Hardening
## 1. Introduction
Some projects are assignments. Others are adventures. My journey into Security Audit and Hardening was the latter—a deep dive into real-world vulnerability assessment, defensive engineering, and fortifying infrastructure against sophisticated digital threats.Over the course of this project, I worked on comprehensively auditing system architecture and systematically hardening critical assets—an initiative to eliminate attack surfaces and transform our baseline security posture into an uncompromised defensive shield. The mission was clear: identify hidden vulnerabilities, enforce strict access controls, and build automated compliance logging into the core pipeline. This wasn’t just about checking off compliance boxes—it was about building proactive resilience into every layer, securing sensitive data payloads, and elevating system trust to production-grade security standards.What follows is not just a technical log, but the story of how an insecure architecture went from vulnerability to absolute validation—complete with structural hurdles, breakthrough mitigations, and defensive design lessons that will outlast the project itself.Thanks to my technical advisors and the engineering team for providing the visibility and support needed to make this infrastructure secure by default.

## 1. Objectives

The primary objective of this project is to strengthen the security posture of OpenELIS by systematically identifying, assessing, prioritizing, and addressing security risks across the application and its development lifecycle. The project is structured around six key objectives.

**O1: Threat Modeling**, focuses on identifying potential attack vectors, trust boundaries, and security risks across the OpenELIS architecture. This will involve analyzing how different components interact, how sensitive data flows through the system, and where attackers could potentially exploit weaknesses. The success of this objective will be measured by the completion of a comprehensive threat model document containing at least ten clearly identified threat scenarios.

**O2: Vulnerability Assessment**, aims to conduct both automated and manual security testing to identify vulnerabilities in the source code, third-party dependencies, infrastructure configurations, and running application. Security testing tools and manual validation techniques will be used to assess critical components of the system. Success will be measured by achieving complete security assessment coverage of critical components and identifying any high-risk vulnerabilities that require remediation.

**O3: Risk Prioritization**, focuses on classifying all identified security issues according to their severity, exploitability, likelihood, and potential business impact. A structured risk assessment process will be used to distinguish critical and high-priority vulnerabilities from medium- and low-priority issues. The expected outcome will be a comprehensive risk matrix containing prioritized findings and a clear remediation plan.

**O4: Security Fixes**, involves implementing targeted patches and improvements for the most significant vulnerabilities identified during the assessment. Where vulnerabilities can be safely reproduced and validated, fixes will be developed, tested, reviewed, and submitted to the OpenELIS project through pull requests. The target is to produce pull requests addressing at least five critical or high-severity security issues, depending on the findings and project scope.

**O5: CI/CD Security Integration**, aims to make security testing a continuous part of the OpenELIS development process rather than a one-time activity. Automated security checks such as static analysis, dependency scanning, and other relevant tests will be integrated into the CI/CD workflow. Success will be measured by ensuring that automated security checks are executed on every relevant pull request.

**O6: Documentation and Community Knowledge Sharing** focuses on ensuring that the knowledge gained during the project benefits the wider OpenELIS community. This will include creating security guidelines, documenting findings and remediation strategies, and sharing the results through community presentations or workshops. The expected outcome is comprehensive security documentation and a knowledge-sharing session that helps contributors maintain and improve the security of the project beyond the duration of the engagement.

## 2. Project Approach and Timeline

The project is designed to run over a period of twelve weeks and is divided into six interconnected phases. Each phase builds upon the work completed in the previous phase, beginning with understanding the OpenELIS architecture and ending with documentation, automation, and community knowledge sharing.

### Phase 1: Assessment and Planning — Weeks 1 and 2

The first phase focuses on understanding the OpenELIS architecture, preparing the development environment, and establishing a structured framework for the security audit. During the first week, the project will begin with onboarding and engagement with the OpenELIS community. The development environment will be configured, relevant architecture documentation will be reviewed, and the major system components and dependencies will be identified. The expected outputs from this initial work include a functioning development environment, an initial architecture diagram showing major components and trust boundaries, and an inventory of critical system components.

During the second week, the scope of the security audit will be defined in collaboration with mentors and the community. Appropriate security testing tools will be selected, and a structured threat-modeling framework will be established. Severity classification criteria will also be defined to ensure that findings can later be prioritized consistently. By the end of this phase, the project will have produced an audit scope document, a proposed security testing toolchain using tools such as OWASP ZAP, SonarQube, Snyk, or suitable alternatives, and a detailed testing plan with a timeline for the remaining project activities.

### Phase 2: Threat Modeling and Vulnerability Scanning — Weeks 3 to 5

The second phase focuses on systematically identifying security risks through architectural analysis, threat modeling, and automated security scanning. During the third week, threat-modeling activities will be conducted to identify important attack surfaces, trust boundaries, and possible security weaknesses. Data flow diagrams will be created for critical workflows, and potential threats will be documented using the STRIDE methodology. The expected deliverables will include a detailed threat model document, data flow diagrams for important workflows, and an initial list of approximately twenty to thirty threat scenarios where applicable.

During the fourth week, static application security testing and dependency vulnerability scanning will be performed on the OpenELIS codebase. The results of these scans will be reviewed carefully to distinguish genuine security concerns from false positives. Dependencies will also be assessed for known vulnerabilities, outdated versions, and other security risks. The main outputs will include static analysis reports, dependency vulnerability reports, and documentation explaining the validation or rejection of significant findings.

The fifth week will focus on dynamic application security testing and manual validation of important security controls. The running application and its API endpoints will be assessed for common security weaknesses. Particular attention will be given to authentication, authorization, access control, input validation, and sanitization. The expected outputs will include dynamic testing reports, an API security assessment, and documented findings relating to input validation and other runtime security controls.

### Phase 3: Risk Prioritization and Analysis — Weeks 6 and 7

The third phase focuses on validating and prioritizing the vulnerabilities and threats identified during the earlier assessment activities. During the sixth week, all findings from threat modeling, static analysis, dependency scanning, and dynamic testing will be reviewed. Significant findings will be manually validated to confirm that they represent genuine security risks. Their exploitability and potential impact on OpenELIS and its users will then be assessed using an appropriate risk-scoring approach, including CVSS where applicable. The main outputs will be a validated vulnerability list and a risk matrix containing severity scores and prioritization information. Proofs of concept may also be developed for safely reproducible vulnerabilities where this is appropriate and useful for demonstrating the issue.

During the seventh week, the validated findings will be prioritized into immediate, short-term, and longer-term remediation categories. A remediation roadmap will be created to distinguish quick wins from more complex architectural or development changes. The findings and proposed priorities will be discussed with project mentors and the OpenELIS community to ensure that the recommendations align with the project's technical architecture and development priorities. The resulting deliverables will include a prioritized remediation plan, an estimated timeline for addressing major issues, and a revised set of findings incorporating community and mentor feedback.

### Phase 4: Security Fixes and Hardening — Weeks 8 to 10

The fourth phase focuses on implementing practical security improvements based on the prioritized findings. During the eighth week, critical vulnerabilities identified during the assessment will be addressed first. Appropriate patches will be implemented, and unit or integration tests will be added where necessary to verify that the vulnerabilities have been resolved and to prevent regressions. The fixes will be documented and submitted to the OpenELIS project as pull requests for community review.

During the ninth week, the project will focus on addressing high-severity vulnerabilities and improving insecure code patterns or configurations. This may involve updating vulnerable dependencies, strengthening security-related configurations, improving HTTP security headers where relevant, and refactoring insecure implementation patterns. The outputs from this work will include additional pull requests, updated dependency configurations, and documentation describing important security configuration improvements.

During the tenth week, remaining time will be used to address selected medium-priority issues and broader security hardening opportunities. Improvements may include stronger input validation, improved logging and monitoring, and regression testing to ensure that implemented fixes do not introduce functional problems. The deliverables will include additional security patches where feasible, enhanced security controls, and regression test results.

### Phase 5: CI/CD Security Integration — Weeks 10 and 11

The fifth phase overlaps with the security hardening phase because security improvements that prove effective should be incorporated into the development workflow as early as possible. During the tenth week, relevant static analysis and dependency scanning tools will be configured for integration into the project's CI pipeline. A security test suite will be established where practical, and clear criteria will be defined for determining when a build or pull request should fail because of a security issue. The expected outcome will be a CI pipeline capable of performing automated security checks, together with documentation describing the security thresholds and build failure criteria.

During the eleventh week, these automated security checks will be integrated into the pull request workflow so that developers receive security feedback during normal development and code review. Additional developer guidance will be created to help contributors understand and resolve reported issues. The pipeline will be tested using representative changes or sample pull requests to confirm that the security checks function correctly. The expected deliverables will include enabled pull request security checks, appropriate project indicators or badges where useful, and a developer security guide explaining how contributors should respond to security findings.

### Phase 6: Documentation and Knowledge Sharing — Weeks 11 and 12

The final phase ensures that the results of the project remain useful to the OpenELIS community after the security audit is completed. During the eleventh week, a comprehensive security audit report will be drafted to document the methodology, findings, risks, remediation efforts, and remaining recommendations. Secure deployment guidance and secure coding practices will also be documented, and presentation materials will be prepared for sharing the results with the community.

During the twelfth and final week, all project documentation will be finalized. The results of the security audit and the implemented improvements will be presented to the OpenELIS community through a meeting, webinar, or other suitable knowledge-sharing session. A blog post or project summary may also be prepared to communicate the outcomes more broadly. Finally, handover documentation will be created to help future contributors continue security improvements. The final outputs will include the completed security audit report, community presentation materials, a project summary or blog post, and handover documentation for future maintainers.

## Deliverables

The first major deliverable, **D1**, will be a threat model document containing a STRIDE-based analysis of the OpenELIS architecture and supporting data flow diagrams. This deliverable is expected by the end of the third week.

The second deliverable, **D2**, will consist of vulnerability assessment reports covering static analysis, dynamic testing, and dependency scanning. These findings will be documented and reviewed by the end of the fifth week.

The third deliverable, **D3**, will be a risk matrix containing validated and prioritized findings, including CVSS scores where applicable. This deliverable is expected by the end of the seventh week.

The fourth deliverable, **D4**, will consist of security patches submitted through pull requests for critical and high-severity vulnerabilities identified during the project. These patches will be developed primarily between weeks eight and ten.

The fifth deliverable, **D5**, will be the integration of automated security testing into the OpenELIS CI/CD pipeline. The goal is to have relevant security checks integrated into the development and pull request workflow by the end of week eleven.

The sixth deliverable, **D6**, will be a comprehensive security audit report summarizing the project methodology, findings, risk analysis, implemented fixes, and recommendations for future improvements. This report will be completed during the twelfth week.

The seventh deliverable, **D7**, will include supporting security documentation such as secure deployment guidance, security configuration recommendations, and secure coding practices. This documentation will also be finalized by the end of week twelve.

The final deliverable, **D8**, will be a community presentation, webinar, or similar knowledge-sharing session in which the project's findings, improvements, and recommendations are presented to the OpenELIS community during the final week.

## Conclusion

This project aims to significantly improve the security posture of OpenELIS by applying a structured and practical approach to security assessment and improvement. The work will combine architectural threat modeling, automated and manual vulnerability assessment, risk prioritization, targeted remediation, and continuous security integration within the development pipeline.

By identifying threats early, validating security findings carefully, and focusing development effort on the highest-priority risks, the project will produce improvements that are both practical and maintainable. Integrating appropriate security checks into the CI/CD workflow will also help ensure that the benefits of the project continue beyond the initial twelve-week period.

The documentation and knowledge-sharing components will further support the OpenELIS community by providing contributors and maintainers with guidance on secure development, deployment, and future security improvements. Ultimately, the project seeks to strengthen the protection of sensitive healthcare information, reduce security risks across the platform, and build greater confidence among users, implementers, and the wider OpenELIS community.

##  References

Key references include the OWASP Application Security Verification Standard, the STRIDE Threat Modeling Methodology, the CVSS version 3.1 specification, OpenELIS architecture and technical documentation, and relevant healthcare data protection and privacy principles, including considerations related to frameworks such as HIPAA and GDPR.

## Future Plans

The GSoC project delivered a stronger and more reliable testing framework, but there are opportunities to take this further. Looking ahead, the following plans will guide continued development:

Expand test coverage further by addressing advanced workflows such as integrations with third-party APIs, mobile responsiveness, and accessibility testing.

Introduce visual regression testing to catch unexpected UI changes that break design consistency.

Enhance CI/CD integration by adding test result dashboards and alerting mechanisms for failed builds.

Explore performance testing integration to ensure not only functional reliability but also speed and scalability under load.

Continue community training and mentorship, ensuring that knowledge about writing and maintaining tests spreads across contributors and doesn’t remain siloed.

## Merged Pull Request Links

https://github.com/DIGI-UW/OpenELIS-Global-2/pull/2779 - add SECURITY.md with vulnerability reporting and security overview

https://github.com/DIGI-UW/OpenELIS-Global-2/pull/3935 - link the SECURITY.md file


## Not Yet Merged.

https://github.com/DIGI-UW/OpenELIS-Global-2/pull/3952 - add Trivy scans, SBOM generation, and image security artifacts for release workflows

### From identifying threats to strengthening defenses, this project transformed security challenges into lasting resilience, making every line of code, every system component, and every deployment a stronger foundation of trust for OpenELIS.
