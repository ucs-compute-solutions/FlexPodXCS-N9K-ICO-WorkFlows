# FlexPodXCS-N9K-ICO-WorkFlows

This repository contains canned Intersight Cloud Orchestrator work-flow for configuring a pair of N9K switching devices. Its expected to have physical connections, required hardware model and NXOS versions have already been setup based on FlexPod latest CVD reccomendations. Also these N9K devices have been claimed to your Intersight account using on-prem Intersight Assit running on your on-prem.
More details can be found out in this FlexPodXCS white papter - 

https://www.cisco.com/c/en/us/products/collateral/servers-unified-computing/ucs-x-series-modular-system/flexpod-xcs-solution-with-intersight-wp.html

Uber work-flow can be imported to your Intersight account using Import feature in Orchestration menu item. Intersight account must have Premier license installed in order to enable Intersight Cloud Orchestrator feature set. Importing uber work-flow alone imports all sub-workflows, custom tasks, config tasks and validation tasks all together. There is no other requirement needed to run the work-flow except giving required inputs during the work-flow exection. 

Uber work-flow for configuring N9k devices for FlexPod based on CVD best practices -

<img width="684" alt="Screen Shot 2022-05-04 at 3 42 39 PM" src="https://user-images.githubusercontent.com/12057795/166837272-f3b9ec59-a028-4da4-a35a-e5c7feb02931.png">

Sub-workflow for enabling features:

<img width="604" alt="Screen Shot 2022-05-04 at 3 44 31 PM" src="https://user-images.githubusercontent.com/12057795/166837410-07d69720-ecef-4b49-a387-07d0e5ae1bfa.png">

Sub-workflow for vLAN configuration:

<img width="641" alt="Screen Shot 2022-05-04 at 3 45 27 PM" src="https://user-images.githubusercontent.com/12057795/166837512-c71348ab-9941-49d7-b6c5-513690a85489.png">

Sub-workflow for vPC configuration:

<img width="524" alt="Screen Shot 2022-05-04 at 3 46 21 PM" src="https://user-images.githubusercontent.com/12057795/166837596-d06aaf81-4327-4a93-8f1f-c307c156bf13.png">

Sub-workflow for Port-Channel configuration:

<img width="642" alt="Screen Shot 2022-05-04 at 3 50 36 PM" src="https://user-images.githubusercontent.com/12057795/166838002-76fd40fd-cc86-4b7f-9bc4-94bd18443156.png">

