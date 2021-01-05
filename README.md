# Dynatrace Maturity Model for Teams

*Note:* 
- This is not an official Dynatrace document. Please treat as such.
- Document creation in progress


![Maturity_Model_Image](./images/maturity_model_plane_2.png)

## Maturity Levels:

### Level 1: Onboard/Start with Dynatrace

### Level 2: Customized Monitoring

### Level 3: 360° Coverage

### Level 4: Events Integration

### Level 5: NoOps

<br>

## Level 1: Onboard/Start with Dynatrace

1. [OneAgent installed](https://www.dynatrace.com/support/help/shortlink/oneagent-hub)
    - [Install using OneAgent package](https://www.dynatrace.com/support/help/shortlink/oneagent-hub#installation-and-operation)
    - Automation
        - [Ansible collection](https://www.dynatrace.com/support/help/shortlink/oneagent-ansible)
        - Chef (coming soon)
        - Puppet (coming soon)

2. [Entities grouped](https://www.dynatrace.com/support/help/shortlink/tags-and-metadata-hub)
    - [HostGroups](https://www.dynatrace.com/support/help/shortlink/host-groups) applied
    - [Metadata](https://www.dynatrace.com/support/help/shortlink/tagging-environment-variable) defined
    - [Tags](https://www.dynatrace.com/support/help/shortlink/tagging) defined
    - [Management Zones](https://www.dynatrace.com/support/help/shortlink/management-zones-hub) defined

3. Hosts, Processes & Services reviewed
    - [Host](https://www.dynatrace.com/support/help/shortlink/hosts-hub) metrics collected - CPU, Mem, Disk, Network etc
    - [Process](https://www.dynatrace.com/support/help/shortlink/processes-hubhttps://www.dynatrace.com/support/help/shortlink/processes-hub) metrics collected - metrics depend on process technology
    - [Services](https://www.dynatrace.com/support/help/shortlink/transactions-and-services-hub) discovered & metrics collected
        - Service Methods detected
        - Service Flow unbroken    

4. [Application(s)](https://www.dynatrace.com/support/help/shortlink/rum-application-concept) setup & reviewed
    - Application created
      - [Application detection rules](https://www.dynatrace.com/support/help/shortlink/application-detection-rules) defined
    - [RUM injection](https://www.dynatrace.com/support/help/shortlink/rum-injection) working
    - [User Session](https://www.dynatrace.com/support/help/shortlink/user-session) reviewed
        -  [User Actions](https://www.dynatrace.com/support/help/shortlink/user-actions) recorded
    - [Async web requests & SPAs](https://www.dynatrace.com/support/help/shortlink/capture-xhr-actions) capture enabled and working

5. [Problem](https://www.dynatrace.com/support/help/shortlink/problem-overview-page) detection reviewed and Alerting setup
    - Auto-generated [Problems](https://www.dynatrace.com/support/help/shortlink/problems-intro) reviewed and [thresholds adjusted](https://www.dynatrace.com/support/help/shortlink/problem-detection-sensitivity) where required
    - [Alerting Profiles](https://www.dynatrace.com/support/help/shortlink/alerting-profiles) setup
    - [Problem Notifications](https://www.dynatrace.com/support/help/shortlink/third-party-integrations-hub) setup
    - [Custom Alerts](https://www.dynatrace.com/support/help/shortlink/event-types-custom-alerts) setup where required

6. Basic health [dashboards](https://www.dynatrace.com/support/help/shortlink/dashboards-hub) created

<br>

## Level 2: Customized Monitoring

1. [Host](https://www.dynatrace.com/support/help/shortlink/hosts-hub)
   - Technology monitoring enabled/disabled per requirement under `Host Settings > General > Monitored Technologies`
   - Process monitoring enabled/eisabled per requirement under `Host Settings > Detected processes`
   - Host anomaly settings adjusted at Host or Host Group level where required. Option available under `Host/HostGroup settings > Anomaly detection`
   - Other Host settings reviewed and adjusted per requirement

2. [Process Group](https://www.dynatrace.com/support/help/shortlink/processes-hubhttps://www.dynatrace.com/support/help/shortlink/processes-hub)
   - Processs Group composition reviewed and [Process Group detection rules](https://www.dynatrace.com/support/help/shortlink/process-groups) created where required
   - [Process Group naming rules](https://www.dynatrace.com/support/help/shortlink/process-group-naming) created/adjusted where required
   - [Process Group availability rules](https://www.dynatrace.com/support/help/shortlink/process-group-alerting) setup
   - [Custom Alerts](https://www.dynatrace.com/support/help/shortlink/event-types-custom-alerts) setup where required

3. [Service](https://www.dynatrace.com/support/help/shortlink/transactions-and-services-hub)
   -  [Service naming rules](https://www.dynatrace.com/support/help/shortlink/custom-service-names) created/adjusted where required
   -  Service url cleanup & request naming rules created/adjusted  under `Service Settings > Web request naming` as required
   -  Service anomaly detection settings adjusted under `Service Settings > Anomaly detection` where required

4. [Application](https://www.dynatrace.com/support/help/shortlink/rum-application-concept)
   -  [User Tags](https://www.dynatrace.com/support/help/shortlink/user-tagging) setup
   -  [User action naming](https://www.dynatrace.com/support/help/shortlink/custom-names) rule setup where required
   -  [Error rules](https://www.dynatrace.com/support/help/shortlink/configure-application-errors) customized where required
   -  Application anomaly detection settings adjusted under `Application settings > Anomaly detection`

<br>

## Level 3: 360° coverage

1. [Synthetic Monitoring](https://www.dynatrace.com/support/help/shortlink/synthetic-hub) of Web pages & APIs setup

2. [Plugins/Extensions](https://www.dynatrace.com/support/help/shortlink/extensions-hub) setup for metrics not monitored out-of-the-box by OneAgents
   -  [Official Dynatrace extensions](https://www.dynatrace.com/support/help/shortlink/other-technologies-subsection#dynatrace-extension-required) setup where required
   -  [Custom Extensions](https://www.dynatrace.com/support/help/shortlink/extensions-hub) capability explored where required

3. [Additional custom events](https://www.dynatrace.com/support/help/shortlink/api-events) sent to Dynatrace where required

4. [SLOs & SLIs](https://www.dynatrace.com/support/help/shortlink/objectives-hub) defined and added to dashboard & alerting

5. Advanced [dashboards](https://www.dynatrace.com/support/help/shortlink/dashboards-hub) created as required

<br>

## Level 4: Events Integration

1. [ITSM/ITOM Integration](https://www.dynatrace.com/support/help/shortlink/third-party-integrations-hub) setup
    - [ServiceNow integration](https://www.dynatrace.com/support/help/shortlink/servicenow)
    - [Jira integration](https://www.dynatrace.com/support/help/shortlink/jira)
    - [OpsGenie integration](https://www.dynatrace.com/support/help/shortlink/opsgenie)
    - [PagerDuty integration](https://www.dynatrace.com/support/help/shortlink/pagerduty)
    - [xMatters integration](https://www.dynatrace.com/support/help/shortlink/id_xmatters-integration)

<br>

## Level 5: NoOps

1. [Load testing tools integration](https://www.dynatrace.com/support/help/shortlink/load-testing-process) setup

1. [Deployment automation](https://www.dynatrace.com/support/help/shortlink/third-party-integrations-hub#deployment-automation) setup
   
2. [Self healing](https://www.dynatrace.com/news/blog/unbreakable-devops-pipeline-shift-left-shift-right-self-healing/) setup

3. Quality gates

4. Automated remediation




