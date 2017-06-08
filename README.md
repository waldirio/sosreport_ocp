Hi

This script will help to do the troubleshooting in OCP / Origin environment, will be possible collect a lot of information about
 - Projects
 - Pods
 - Detailed descriptions
 - and much more

At the end will be generated one tar that should be send to the Support Team.

To Execute the script., just download and execute

./sosreport_ocp

The script will collect a lot of information about OCP and will store everything on dir /tmp/ocp/ocp_report_<date and time>

At the end you will see one message like below

~~~
Compacting logs
tar cpf /tmp/ocp/ocp_report_06.07.17-20.15.tar /tmp/ocp/ocp_report_06.07.17-20.15
tar: Removing leading `/' from member names

Please attach the file below to the case
/tmp/ocp/ocp_report_06.07.17-20.15.tar
~~~

Then just send this file to the Support Team.

Below the structure generated.

~~~
# tree /tmp/ocp/ocp_report_06.07.17-20.15
/tmp/ocp/ocp_report_06.07.17-20.15
|-- oc_get_nodes
|-- oc_get_pods
|-- oc_get_projects
`-- projects
    |-- default
    |   |-- actual_connection
    |   |-- connection_status
    |   |-- oc_describe_pod_docker-registry-1-6t349
    |   |-- oc_describe_pod_registry-console-1-1h752
    |   |-- oc_describe_pod_router-1-0m2pm
    |   `-- oc_get_pods
    |-- kube-system
    |   |-- actual_connection
    |   |-- connection_status
    |   `-- oc_get_pods
    |-- logging
    |   |-- actual_connection
    |   |-- connection_status
    |   `-- oc_get_pods
    |-- management-infra
    |   |-- actual_connection
    |   |-- connection_status
    |   `-- oc_get_pods
    |-- openshift
    |   |-- actual_connection
    |   |-- connection_status
    |   `-- oc_get_pods
    |-- openshift-infra
    |   |-- actual_connection
    |   |-- connection_status
    |   `-- oc_get_pods
    `-- orange
        |-- actual_connection
        |-- connection_status
        |-- oc_describe_pod_cake-1-34ljb
        |-- oc_describe_pod_cake-1-build
        |-- oc_describe_pod_cake-1-fdt65
        `-- oc_get_pods

8 directories, 30 files
#
~~~
