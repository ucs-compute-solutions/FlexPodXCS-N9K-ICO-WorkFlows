# Intersight Orchestrator work-flow for configuring N9K devices for FlexPod

This repository contains canned Intersight Cloud Orchestrator work-flow for configuring a pair of N9K ethernet switching devices required for FlexPod reference architeture implementation. Its expected to have physical connections, required hardware model and NXOS versions have already been setup based on FlexPod latest CVD reccomendations. Also these N9K devices have been claimed to your Intersight account using on-prem Intersight Assist running on your on-prem.
More details can be found out in this FlexPodXCS white papter - 

https://www.cisco.com/c/en/us/products/collateral/servers-unified-computing/ucs-x-series-modular-system/flexpod-xcs-solution-with-intersight-wp.html

Uber work-flow can be imported to your Intersight account using Import feature in Orchestration menu. Intersight account must have premier license installed in order to enable Intersight Cloud Orchestrator feature set. Importing uber work-flow alone, imports all sub-workflows, custom tasks, config tasks, parallel loop tasks, conditional tasks and validation tasks all together. There is no other requirement needed to run the work-flow except giving required inputs during the work-flow execution. 

<img width="1511" alt="Screen Shot 2022-05-04 at 4 20 16 PM" src="https://user-images.githubusercontent.com/12057795/166840700-5e0344bf-ca77-4fd7-9271-711e31042867.png">


Uber work-flow for configuring N9k devices for FlexPod based on CVD best practices -

<img width="684" alt="Screen Shot 2022-05-04 at 3 42 39 PM" src="https://user-images.githubusercontent.com/12057795/166837272-f3b9ec59-a028-4da4-a35a-e5c7feb02931.png">

Sub-workflow for enabling features:

Following features will be enabled through this sub-workflow -

enabled_features:
  - lacp
  - vpc
  - interface-vlan
  - nxapi
  - udld
  - lldp

  <img width="604" alt="Screen Shot 2022-05-04 at 3 44 31 PM" src="https://user-images.githubusercontent.com/12057795/166837410-07d69720-ecef-4b49-a387-07d0e5ae1bfa.png">

Sub-workflow for global settings:

Following STP & LB settings get configured by this sub-workflow -

global_settings:
  - spanning-tree port type network default
  - spanning-tree port type edge bpduguard default
  - spanning-tree port type edge bpdufilter default
  - port-channel load-balance src-dst l4port
  - system default switchport
  - system default switchport shutdown

  <img width="685" alt="Screen Shot 2022-05-04 at 4 21 45 PM" src="https://user-images.githubusercontent.com/12057795/166840978-826918f2-3275-4096-bb5a-aecf2e1731d8.png">

Sub-workfloe for NTP configuration:
  
  <img width="645" alt="Screen Shot 2022-05-04 at 4 42 13 PM" src="https://user-images.githubusercontent.com/12057795/166842448-015a26eb-acd4-4047-aaa5-2b605d04b509.png">
  
  Sub-workflow for vLAN configuration:

  <img width="641" alt="Screen Shot 2022-05-04 at 3 45 27 PM" src="https://user-images.githubusercontent.com/12057795/166837512-c71348ab-9941-49d7-b6c5-513690a85489.png">

  Sub-workflow for vPC configuration:

  <img width="524" alt="Screen Shot 2022-05-04 at 3 46 21 PM" src="https://user-images.githubusercontent.com/12057795/166837596-d06aaf81-4327-4a93-8f1f-c307c156bf13.png">

  Sub-workflow for Port-Channel configuration:

  <img width="642" alt="Screen Shot 2022-05-04 at 3 50 36 PM" src="https://user-images.githubusercontent.com/12057795/166838002-76fd40fd-cc86-4b7f-9bc4-94bd18443156.png">

