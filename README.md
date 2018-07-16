# aws-cf-vpc-endpoint-service-azs
Look up the Availability Zones associated with the VPC endpoint of an AWS service.

AWS services that offer interface endpoints present Elastic Network Interfaces on
subnets within some, but not necessarily all, regions within Availability Zones (AZs).
This CloudFormation template defines a custom resource backed by a Python 3 Lambda
function to look up the AZs that offer interface endpoints for a service. The function
accepts two arguments, a service name and the desired (e.g. minimum) number of AZs
offering such endpoints.   The function returns the actual number of AZs that offer
the endpoints and a comma-separated list of the AZs. The example within the file also
shows how to look up the AZs offering interface endpoints for AWS Secrets Manager.

The standard disclaimer applies:  I am not speaking on behalf of AWS.
