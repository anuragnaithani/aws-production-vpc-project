# Commands Used

## Copy PEM file to Bastion Host

```bash
scp -i demo-website-aws.pem demo-website-aws.pem ubuntu@BASTION_PUBLIC_IP:/home/ubuntu
```

## SSH into Bastion Host

```bash
ssh -i demo-website-aws.pem ubuntu@BASTION_PUBLIC_IP
```

## SSH into Private EC2

```bash
ssh -i demo-website-aws.pem ubuntu@PRIVATE_EC2_IP
```

## Create Website

```bash
cat > index.html <<EOF2
<!DOCTYPE html>
<html>
<body>
<h1>My First AWS Project</h1>
<p>Application running in private subnet</p>
</body>
</html>
EOF2
```

## Run Python Server

```bash
python3 -m http.server 8000
```
