# Business Process Plaform
Business process platform is a reference architecture demonstration built on Microsoft low-code product Power Platform. 

## Purpose
1. Demonstrate how to leverage the full capability of Power Platform to build a centralized process solution including a server side platform and a sample client
2. By designing this process platform to decrease delivery effort and cost for enterprise, meanwhile increase process operation efficiency.

## Principle of design
1.Abstract the process pattern to build a describable process rule. 
![image](https://github.com/illusion615/businessprocessplaform/assets/239253/0ba9224f-4fa1-4bed-8844-12564573777a)

2. centralize the process design and operation in one single platform rather than seperate business application, a sort like BPM.

4. Isolate the process data and logic from business data to maximize the resuability of this platform.
![image](https://github.com/illusion615/businessprocessplaform/assets/239253/37d7409b-f3f3-4ccb-8cf8-48424a1339a5)

6. To support wide range of client application, not limit to Power Platform low-code applications, also provide the WebAPI to support 3rd party applications.
![image](https://github.com/illusion615/businessprocessplaform/assets/239253/166e032b-5f8a-4d50-b887-206fc7c730df)

## Arhitecture
![image](https://github.com/illusion615/businessprocessplaform/assets/239253/a8351907-55f0-4765-993c-04df2d3b389f)

## Flow Sequence
![image](https://github.com/illusion615/businessprocessplaform/assets/239253/eadbbb8c-89d9-412d-9963-97f0242c49ef)

## Screenshot
### Process Platform Server
#### Process dashboard
![image](https://github.com/illusion615/businessprocessplaform/assets/239253/ced911b5-5b1c-4802-b0bc-a3c9f6758bbd)

#### Process template setup
![image](https://github.com/illusion615/businessprocessplaform/assets/239253/5640e754-2e42-4896-ae1a-4fdf6b070d14)

![image](https://github.com/illusion615/businessprocessplaform/assets/239253/ee7a4db1-91c8-4dfb-8c6c-0798050a417b)

#### Process instance
![image](https://github.com/illusion615/businessprocessplaform/assets/239253/0a43fc63-ce0e-476e-9c2e-bd32b56b3832)
### Process client demo
![image](https://github.com/illusion615/businessprocessplaform/assets/239253/f973114f-d5cb-472a-93ac-02133233a5af)

## Deployment
The solution requires at least 1 environment with Dataverse enabled for Process Platform Server solution. and client environment by your client application requirement.

### Process Platform Server

#### License Requirement
- Power Apps per User License for all process participants
- Powwer Automate Process(Based on process volumn)
  
#### Environment Feature Requirement
- Dataverse enabled
- Currently support locailzation for language English(1033) and Simplified Chinese(2052)
- PCF enabled

#### Installzation
1. Download and deploy below prerequiest solution package
1.1. Creator Kit
1.2. FormatJSONControl
2. Download the latest process platform solution package and import
3. Publish all
4. Process data initialization and setup
5. Note down below WebAPI's URL for further client config
5.1. WebAPI - Query Process Status
5.2. WebAPI - Get User's BU Info
5.3. WebAPI - Initiate Process
5.4. WebAPI - Query Process Status

### Process Client Sample
#### License Requirement
- Power Apps per App/per User for all application users

#### Environment Feature Requirements
- Dataverse enabled
- Currently support locailzation for language English(1033) and Simplified Chinese(2052)
- PCF enabled

#### Installzation
1. Download and deploy below prerequiest solution package
1.1. Creator Kit
1.2. FormatJSONControl
1.3. PcfFormJson
3. Download the latest Business Process Accelaerator - Sample Client solution package and import
4. Publish all
5. Configure the environment variable "Rule Based Process Platform WebAPI Connections"
   
## Change log

