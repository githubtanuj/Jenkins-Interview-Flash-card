# Jenkins-Interview-Questions-Flash-card

Q1: What is Jenkins?
A1: Jenkins is an open-source CI/CD tool that automates build, test, and deployment.

Q2: What are the main features of Jenkins?
A2: Free, 2000+ plugins, pipeline as code, distributed builds, easy setup.

Q3: What are the advantages of Jenkins?
A3: Speeds up delivery, automates CI/CD, supports most tools, customizable.

Q4: Name some important Jenkins plugins.
A4: Git, Pipeline, Blue Ocean, Docker, JUnit, Email, AnsiColor.

Q5: What is Continuous Integration (CI) in Jenkins?
A5: Auto build/test code when pushed to version control to detect bugs early.

Q6: What is the difference between Hudson and Jenkins?
A6: Jenkins is a fork of Hudson with more community support; Hudson is outdated.

Q7: What is Groovy used for in Jenkins?
A7: Used to script pipelines and shared libraries.

Q8: What command starts Jenkins?
A8: java -jar jenkins.war or sudo systemctl start jenkins

Q9: What is a Jenkinsfile?
A9: A file (in source control) that defines the pipeline in code.

Q10: Difference between CI, CD (Delivery), and CD (Deployment)?
A10:

CI: Auto build/test


CD: Deploy to staging


CD Deployment: Auto deploy to production


Q11: What is a Jenkins Pipeline?
A11: A series of automated steps (build/test/deploy) written in Jenkinsfile.

Q12: What is a Scripted Pipeline?
A12: Pipeline written in Groovy with full control and flexibility.

Q13: What is a Declarative Pipeline?
A13: Simpler structured syntax, easier to read and maintain.

Q14: Which SCM tools are supported in Jenkins?
A14: Git, SVN, Mercurial, Perforce.

Q15: Which CI tools can Jenkins integrate with?
A15: GitLab CI, Travis, CircleCI, Maven, Gradle.

Q16: How can Jenkins be started manually?
A16:

CLI: java -jar jenkins.war


Web: /safeRestart, /restart


Q17: What are Environment Directives in Jenkins?
A17: Used to set environment variables inside pipeline.

Q18: What are triggers in Jenkins?
A18: Events that start builds (SCM push, cron, webhooks, upstream jobs).

Q19: What is the Agent directive in Jenkins?
A19: Defines where (which node/container) the pipeline or stage runs.

Q20: How to prevent build failures in Jenkins?
A20: Test locally, use small commits, static analysis, automation.

Q21: Difference between Maven, Ant, and Jenkins?
A21:

Maven/Ant: Build tools


Jenkins: CI/CD automation server


Q22: What is the 'post' section in Jenkins pipeline?
A22: Runs steps after pipeline (e.g., always, failure, success).

Q23: What are parameters in Jenkins?
A23: User-defined inputs passed before build (string, choice, etc.).

Q24: How to create a Jenkins job?
A24: New Item → Choose type → Set SCM, build steps → Save.

Q25: Two key integrations Jenkins requires?
A25:

SCM tool (Git)


Build tool (Maven/Gradle)


Q26: How to clone a Git repo in Jenkins?
A26: Use Git plugin and add the repo URL in SCM section of job config.

Q27: How to secure Jenkins?
A27: Use RBAC, credentials plugin, HTTPS, regular updates.

Q28: How to back up Jenkins?
A28: Backup $JENKINS_HOME or use ThinBackup plugin.

Q29: What is the Backup plugin?
A29: ThinBackup helps schedule and manage Jenkins backups via UI.

Q30: What is Flow Control in Jenkins?
A30: Manages logic using when, input, timeout, if.

Q31: How to fix broken builds?
A31: Check logs, test locally, rollback changes, validate environment.

Q32: What are the requirements to install Jenkins?
A32: Java 8+, 2GB+ RAM, 10GB+ disk, Linux/Windows/macOS.

Q33: Describe a simple CD workflow.
A33: Code → Build → Test → Deploy to staging → Manual approval → Prod.

Q34: Ways to schedule builds in Jenkins?
A34: Poll SCM, Cron syntax, Webhook, Manual trigger.

Q35: Why is Jenkins a CD tool?
A35: Automates end-to-end deployment pipeline.

Q36: Give a simple pipeline example.
A36:
pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
  }
}
