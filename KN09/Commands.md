1. VPC erstellen
```
aws ec2 create-vpc --cidr-block 10.0.0.0/16 --tag-specifications ResourceType=vpc,Tags=[{Key=Name,Value=vpc-kn05}]
```

2. Subnetz erstellen
```
aws ec2 create-subnet --vpc-id vpc-081ec835f3EXAMPLE --cidr-block 10.0.1.0/24 --tag-specifications ResourceType=subnet,Tags=[{Key=Name,Value=subnet-kn05}]
```

3. Internet Gateway erstellen
```
aws ec2 create-internet-gateway --tag-specifications ResourceType=internet-gateway,Tags=[{Key=Name,Value=igw-kn05}]
```

4. Internet Gateway an VPC anhängen
```
aws ec2 attach-internet-gateway --vpc-id vpc-081ec835f3EXAMPLE --internet-gateway-id igw-0abcd1234EXAMPLE
```

5. Route Table erstellen
```
aws ec2 create-route-table --vpc-id vpc-081ec835f3EXAMPLE --tag-specifications ResourceType=route-table,Tags=[{Key=Name,Value=rt-kn05}]
```

6. Route zu Internet Gateway hinzufügen
```
aws ec2 create-route --route-table-id rtb-0abcd1234EXAMPLE --destination-cidr-block 0.0.0.0/0 --gateway-id igw-0abcd1234EXAMPLE
```

7. Route Table dem Subnetz zuordnen
```
aws ec2 associate-route-table --subnet-id subnet-0abcd1234EXAMPLE --route-table-id rtb-0abcd1234EXAMPLE
```

8. Sicherheitsgruppe erstellen
```
aws ec2 create-security-group --group-name sg-kn05 --description "Security Group for KN09" --vpc-id vpc-081ec835f3EXAMPLE
```

9. Regel für eingehenden Datenbankverkehr hinzufügen
```
aws ec2 authorize-security-group-ingress --group-id sg-0abcd1234EXAMPLE --protocol tcp --port 3306 --cidr 0.0.0.0/0
```

10. EC2-Instanz erstellen
```
aws ec2 run-instances --image-id ami-0c55b159cbfafe1f0 --count 1 --instance-type t2.micro
```

### B) Terraform (70%)
```
terraform init
terraform apply
```
