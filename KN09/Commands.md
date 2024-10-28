### Instanz stoppen
aws ec2 stop-instances --instance-ids i-01bafbf2e2ceb1407 
### Instanz Starten
aws ec2 start-instances --instance-ids i-01bafbf2e2ceb1407
### Instanz erstellen
aws ec2 run-instances --image-id ami-0866a3c8686eaeeba --count 1 --instance-type t2.micro --key-name Max1 --security-group-ids sg-0b555fb54b35c6661 --subnet-id subnet-071ca88343e4f9fb4 --user-data file://C:\Users\sussy\Downloads\cloud-config.yaml


