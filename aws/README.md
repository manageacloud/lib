# Amazon Web Services

## Autoscaled application

`aws-autoscale.abstract.macfile` creates the following elements in aws:

 - An instance that that contains the software
 - A load balancer
 - The instance is registered in the load balancer
 - An image is created from the instance
 - Creates a launch configuration
 - Creates an autoscale group
 - Creates two scale policies, to add servers and to remove servers
 - Creates two CloudWatch alerts, used to for the scale policy up and down
 
 
`aws-autoscale.demo.macfile` contains a demo for this application. You can use it as boiler plate for similar applications.
 
To run the demo to create an autoscaled application run. Please note that this demo requires [aws cli](http://docs.aws.amazon.com/cli/latest/userguide/installing.html) and [ManageaCloud](https://manageacloud.com/docs/getting-started/install) configured.
 
```sh
mac -s infrastructure macfile https://github.com/manageacloud/lib/blob/master/aws/aws-autoscale.demo.macfile -p INF_NAME=demo INF_VERSION=1 AWS_REGION=us-east-1
```

To destroy all the resources that has been created:
```sh
mac -s infrastructure destroy demo 1
```

 
 