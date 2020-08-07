### VD8F-Verify application availability when node is powered off.

#### Description

This test fails a node by shutting it down and checks if the application is rescheduled and verify its availability.

#### Prerequisites

- OpenShift Cluster should be created and have the dependencies installed.
- cStor based storage pool should have been created.
- OpenEBS storage class should be created with the desired storage pool claim.

#### Procedure

- This job triggers the litmus experiments which reboots a node on vmware server and verify if the application is scheduled on other node.
- The litmus experiment receives the necessary parameters in form of pod environmental variables and updates the manifest files accordingly.
- It deploys an application using cstor storage engine and dumps data into it.
- Then it fails the node where application is running and check if application is rescheduled and verify its availability.
- Finally, it deprovisions the application and update the result.

#### Expected result

- Application should be scheduled on some other node.

#### Test Result


| Job ID |   Test Description         | Execution Time |Test Result   |
 |---------|---------------------------| --------------|--------|
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/102221">102221</a>           |  Fail the node where the application is running and check the behaviour           | Fri Oct 25 14:33:20 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:'2690745634bc5d1c5b2d20c8d98392c1d20b1f98',type:phrase),type:phrase,value:'2690745634bc5d1c5b2d20c8d98392c1d20b1f98'),query:(match:(commit_id:(query:'2690745634bc5d1c5b2d20c8d98392c1d20b1f98',type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:'3729',type:phrase),type:phrase,value:'3729'),query:(match:(pipeline_id:(query:'3729',type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/100524">100524</a>           |  Fail the node where the application is running and check the behaviour           | Fri Oct 18 14:17:18 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:'f5363c4bfb3687c9b2f529156aec92921d0a434f',type:phrase),type:phrase,value:'f5363c4bfb3687c9b2f529156aec92921d0a434f'),query:(match:(commit_id:(query:'f5363c4bfb3687c9b2f529156aec92921d0a434f',type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:'3682',type:phrase),type:phrase,value:'3682'),query:(match:(pipeline_id:(query:'3682',type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/95053">95053</a>           |  Fail the node where the application is running and check the behaviour           | Thu Oct 10 17:09:51 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:'0ee224280e309e148f70d30fbfde8b9dbd3af1e5',type:phrase),type:phrase,value:'0ee224280e309e148f70d30fbfde8b9dbd3af1e5'),query:(match:(commit_id:(query:'0ee224280e309e148f70d30fbfde8b9dbd3af1e5',type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:'3522',type:phrase),type:phrase,value:'3522'),query:(match:(pipeline_id:(query:'3522',type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/94872">94872</a>           |  Fail the node where the application is running and check the behaviour           | Thu Oct 10 12:51:45 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:'b315cedbd1d09b900f6e940434a180608c4ef2a3',type:phrase),type:phrase,value:'b315cedbd1d09b900f6e940434a180608c4ef2a3'),query:(match:(commit_id:(query:'b315cedbd1d09b900f6e940434a180608c4ef2a3',type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:'3515',type:phrase),type:phrase,value:'3515'),query:(match:(pipeline_id:(query:'3515',type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/94123">94123</a>           |  Fail the node where the application is running and check the behaviour           | Wed Oct  9 21:19:28 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:'b315cedbd1d09b900f6e940434a180608c4ef2a3',type:phrase),type:phrase,value:'b315cedbd1d09b900f6e940434a180608c4ef2a3'),query:(match:(commit_id:(query:'b315cedbd1d09b900f6e940434a180608c4ef2a3',type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:'3493',type:phrase),type:phrase,value:'3493'),query:(match:(pipeline_id:(query:'3493',type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/93516">93516</a>           |  Fail the node where the application is running and check the behaviour           | Wed Oct  9 14:33:22 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:'b315cedbd1d09b900f6e940434a180608c4ef2a3',type:phrase),type:phrase,value:'b315cedbd1d09b900f6e940434a180608c4ef2a3'),query:(match:(commit_id:(query:'b315cedbd1d09b900f6e940434a180608c4ef2a3',type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:'3475',type:phrase),type:phrase,value:'3475'),query:(match:(pipeline_id:(query:'3475',type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/92705">92705</a>           |  Fail the node where the application is running and check the behaviour           | Fri Oct  4 21:25:27 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:'ba53f6de2bb05055e796b6ea1fdde9015ccd2ad1',type:phrase),type:phrase,value:'ba53f6de2bb05055e796b6ea1fdde9015ccd2ad1'),query:(match:(commit_id:(query:'ba53f6de2bb05055e796b6ea1fdde9015ccd2ad1',type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:'3449',type:phrase),type:phrase,value:'3449'),query:(match:(pipeline_id:(query:'3449',type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/92286">92286</a>           |  Fail the node where the application is running and check the behaviour           | Fri Oct  4 02:26:00 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:'2a68a33c5fb6fff050dd3a4909213d355b51f020',type:phrase),type:phrase,value:'2a68a33c5fb6fff050dd3a4909213d355b51f020'),query:(match:(commit_id:(query:'2a68a33c5fb6fff050dd3a4909213d355b51f020',type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:'3432',type:phrase),type:phrase,value:'3432'),query:(match:(pipeline_id:(query:'3432',type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/91825">91825</a>           |  Fail the node where the application is running and check the behaviour           | Thu Oct  3 20:52:55 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:'2a68a33c5fb6fff050dd3a4909213d355b51f020',type:phrase),type:phrase,value:'2a68a33c5fb6fff050dd3a4909213d355b51f020'),query:(match:(commit_id:(query:'2a68a33c5fb6fff050dd3a4909213d355b51f020',type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:'3419',type:phrase),type:phrase,value:'3419'),query:(match:(pipeline_id:(query:'3419',type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/90710">90710</a>           |  Fail the node where the application is running and check the behaviour           | Thu Oct  3 12:50:04 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:'2a68a33c5fb6fff050dd3a4909213d355b51f020',type:phrase),type:phrase,value:'2a68a33c5fb6fff050dd3a4909213d355b51f020'),query:(match:(commit_id:(query:'2a68a33c5fb6fff050dd3a4909213d355b51f020',type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:'3388',type:phrase),type:phrase,value:'3388'),query:(match:(pipeline_id:(query:'3388',type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/90392">90392</a>           |  Fail the node where the application is running and check the behaviour           | Mon Sep 30 23:00:36 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:'2a68a33c5fb6fff050dd3a4909213d355b51f020',type:phrase),type:phrase,value:'2a68a33c5fb6fff050dd3a4909213d355b51f020'),query:(match:(commit_id:(query:'2a68a33c5fb6fff050dd3a4909213d355b51f020',type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:'3379',type:phrase),type:phrase,value:'3379'),query:(match:(pipeline_id:(query:'3379',type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
 |    <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/89706">89706</a>   |  Fail the node where the application is running and check the behaviour           |  Thu Sep 26 19:23:24 IST 2019     |<a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:'4d9704a87a0a9f0b1b8947f5825957948dba35de',type:phrase),type:phrase,value:'4d9704a87a0a9f0b1b8947f5825957948dba35de'),query:(match:(commit_id:(query:'4d9704a87a0a9f0b1b8947f5825957948dba35de',type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:'3355',type:phrase),type:phrase,value:'3355'),query:(match:(pipeline_id:(query:'3355',type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a>  |