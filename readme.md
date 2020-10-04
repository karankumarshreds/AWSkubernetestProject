Steps involved : 

- Install AWS tools for windows 

```
> Install-Module -Name AWS.Tools.Common
```

- Downlaod AWS CLI installer and restart terminal

```
> aws --version
```

- Configure credentials and add in Access key and Secret key

```
> aws configure
```
### Below commands are given by ecr only after creating a repository, we just have to copy-paste them : 

- Login to your ecr repository: 

```
> aws ecr get-login-password | docker login --username AWS --password-stdin 995054106418.dkr.ecr.us-east-2.amazonaws.com
```

- Build the image: 

```
> docker build -t nodejs .
```

- After the build completes, tag your image so you can push the image to this repository:

```
> docker tag nodejs:latest 995054106418.dkr.ecr.us-east-2.amazonaws.com/nodejs:latest
```

- Run the following command to push this image to your newly created AWS repository:

```
> docker push 995054106418.dkr.ecr.us-east-2.amazonaws.com/nodejs:latest

```

## Autoscaling 

```
> kubectl autoscale deployment node-depl --cpu-percent=50  --min=7 --max=10
```
