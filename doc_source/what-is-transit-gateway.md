# What is a Transit Gateway?<a name="what-is-transit-gateway"></a>

A *transit gateway* is a network transit hub that you can use to interconnect your virtual private clouds \(VPC\) and on\-premises networks\.

For more information, see [AWS Transit Gateway](https://aws.amazon.com/transit-gateway)\.

## Transit Gateway Concepts<a name="concepts"></a>

The following are the key concepts for transit gateways:
+ **attachment** — You can attach a VPC or VPN connection to a transit gateway\.
+ **transit gateway route table** — A transit gateway has a default route table and can optionally have additional route tables\. A route table includes dynamic and static routes that decide the next hop based on the destination IP address of the packet\. The target of these routes could be a VPC or a VPN connection\. By default, the VPCs and VPN connections that you attach to a transit gateway are associated with the default transit gateway route table\.
+ **associations** — Each attachment is associated with exactly one route table\. Each route table can be associated with zero to many attachments\.
+ **route propagation** — A VPC or VPN connection can dynamically propagate routes to a transit gateway route table\. With a VPC, you must create static routes to send traffic to the transit gateway\. With a VPN connection, routes are propagated from the transit gateway to your on\-premises router using Border Gateway Protocol \(BGP\)\.

## Working with Transit Gateways<a name="tgw-interfaces"></a>

You can create, access, and manage your transit gateways using any of the following interfaces:
+ **AWS Management Console**— Provides a web interface that you can use to access your transit gateways\.
+ **AWS Command Line Interface \(AWS CLI\)** — Provides commands for a broad set of AWS services, including Amazon VPC, and is supported on Windows, Mac, and Linux\. For more information, see [AWS Command Line Interface](https://aws.amazon.com//cli/)\.
+ **AWS SDKs** — Provides language\-specific APIs and takes care of many of the connection details, such as calculating signatures, handling request retries, and error handling\. For more information, see [AWS SDKs](http://aws.amazon.com/tools/#SDKs)\.
+ **Query API**— Provides low\-level API actions that you call using HTTPS requests\. Using the Query API is the most direct way to access Amazon VPC, but it requires that your application handle low\-level details such as generating the hash to sign the request, and error handling\. For more information, see the [Amazon EC2 API Reference](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/)\.

## Pricing<a name="pricing"></a>

You are charged based on each hour that your VPC or VPN connection are attached to the transit gateway\. For more information, see [AWS Transit Gateway pricing](https://aws.amazon.com/transit-gateway)\.