# Instanz gestoppt
![image](https://github.com/user-attachments/assets/e964f832-5cce-460c-a58a-039cc98df0cb)

# Instanz gestartet
![image](https://github.com/user-attachments/assets/53078823-fc0e-43a4-8d48-b6196c773b55)

# Neue Instanz erstellt
![image](https://github.com/user-attachments/assets/839d05f5-0175-4e86-8fc3-db4858defa74)
Output im CMD:
```
{
    "ReservationId": "r-0091c3acbd8d01533",
    "OwnerId": "065613351264",
    "Groups": [],
    "Instances": [
        {
            "Architecture": "x86_64",
            "BlockDeviceMappings": [],
            "ClientToken": "ce0b3f9d-a47b-4d13-996d-fbdb648dd015",
            "EbsOptimized": false,
            "EnaSupport": true,
            "Hypervisor": "xen",
            "NetworkInterfaces": [
                {
                    "Attachment": {
                        "AttachTime": "2024-10-28T16:30:52+00:00",
                        "AttachmentId": "eni-attach-0da3651d06f801528",
                        "DeleteOnTermination": true,
                        "DeviceIndex": 0,
                        "Status": "attaching",
                        "NetworkCardIndex": 0
                    },
                    "Description": "",
                    "Groups": [
                        {
                            "GroupId": "sg-0b555fb54b35c6661",
                            "GroupName": "launch-wizard-37"
                        }
                    ],
                    "Ipv6Addresses": [],
                    "MacAddress": "0e:4f:d9:ce:a1:f1",
                    "NetworkInterfaceId": "eni-00570ec0c9b6d68f5",
                    "OwnerId": "065613351264",
                    "PrivateDnsName": "ip-172-31-35-136.ec2.internal",
                    "PrivateIpAddress": "172.31.35.136",
                    "PrivateIpAddresses": [
                        {
                            "Primary": true,
                            "PrivateDnsName": "ip-172-31-35-136.ec2.internal",
                            "PrivateIpAddress": "172.31.35.136"
                        }
                    ],
                    "SourceDestCheck": true,
                    "Status": "in-use",
                    "SubnetId": "subnet-071ca88343e4f9fb4",
                    "VpcId": "vpc-0d8382a10aa9fc130",
                    "InterfaceType": "interface"
                }
            ],
            "RootDeviceName": "/dev/sda1",
            "RootDeviceType": "ebs",
            "SecurityGroups": [
                {
                    "GroupId": "sg-0b555fb54b35c6661",
                    "GroupName": "launch-wizard-37"
                }
            ],
            "SourceDestCheck": true,
            "StateReason": {
                "Code": "pending",
                "Message": "pending"
            },
            "VirtualizationType": "hvm",
            "CpuOptions": {
                "CoreCount": 1,
                "ThreadsPerCore": 1
            },
            "CapacityReservationSpecification": {
                "CapacityReservationPreference": "open"
            },
            "MetadataOptions": {
                "State": "pending",
                "HttpTokens": "required",
                "HttpPutResponseHopLimit": 2,
                "HttpEndpoint": "enabled",
                "HttpProtocolIpv6": "disabled",
                "InstanceMetadataTags": "disabled"
            },
            "EnclaveOptions": {
                "Enabled": false
            },
            "BootMode": "uefi-preferred",
            "PrivateDnsNameOptions": {
                "HostnameType": "ip-name",
                "EnableResourceNameDnsARecord": false,
                "EnableResourceNameDnsAAAARecord": false
            },
            "MaintenanceOptions": {
                "AutoRecovery": "default"
            },
            "CurrentInstanceBootMode": "legacy-bios",
            "InstanceId": "i-0ef70bb2e924dca68",
            "ImageId": "ami-0866a3c8686eaeeba",
            "State": {
                "Code": 0,
                "Name": "pending"
            },
            "PrivateDnsName": "ip-172-31-35-136.ec2.internal",
            "PublicDnsName": "",
            "StateTransitionReason": "",
            "KeyName": "Max1",
            "AmiLaunchIndex": 0,
            "ProductCodes": [],
            "InstanceType": "t2.micro",
            "LaunchTime": "2024-10-28T16:30:52+00:00",
            "Placement": {
                "GroupName": "",
                "Tenancy": "default",
                "AvailabilityZone": "us-east-1b"
            },
            "Monitoring": {
                "State": "disabled"
            },
            "SubnetId": "subnet-071ca88343e4f9fb4",
            "VpcId": "vpc-0d8382a10aa9fc130",
            "PrivateIpAddress": "172.31.35.136"
        }
    ]
}
```



