# Transit Gateway VPN Attachments<a name="tgw-vpn-attachments"></a>

To attach a VPN connection to your transit gateway, you must specify the customer gateway\.

For static VPNs, add the static routes to the transit gateway route table\.

## Create a Transit Gateway Attachment to a VPN<a name="create-vpn-attachment"></a>

**To create a VPN attachment using the console**

1. Open the Amazon VPC console at [https://console\.aws\.amazon\.com/vpc/](https://console.aws.amazon.com/vpc/)\.

1. On the navigation pane, choose **Transit Gateway Attachments**\.

1. Choose **Create Transit Gateway Attachment**\.

1. For **Transit Gateway ID**, choose the transit gateway for the attachment\. You can choose a transit gateway that you own or a transit gateway that was shared with you\.

1. For **Attachment type**, choose **VPN**\.

1. For **Customer Gateway**, do one of the following:
   + To use an existing customer gateway, choose **Existing**, and then select the gateway to use\.

     If your customer gateway is behind a network address translation \(NAT\) device that's enabled for NAT traversal \(NAT\-T\), use the public IP address of your NAT device, and adjust your firewall rules to unblock UDP port 4500\.
   + To create a customer gateway, choose **New**, then for **IP Address**, type a static public IP address and **BGP ASN**\.

     For **Routing options**, choose whether to use **Dynamic** or **Static**\.

1. For **Tunnel Options**, see [VPN Routing Options](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_VPN.html#VPNRoutingTypes)\.

1. For **Inside IP CIDR**, see [Configuring the VPN Tunnels for Your VPN Connection](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_VPN.html#VPNTunnels)\.

1. Choose **Create attachment**\.

**To create a VPN attachment using the AWS CLI**  
Use the [create\-vpn\-connection](https://docs.aws.amazon.com/cli/latest/reference/ec2/create-vpn-connection.html) command\.

## View Your VPN Attachments<a name="view-vpn-attachment"></a>

**To view your VPN attachments using the console**

1. Open the Amazon VPC console at [https://console\.aws\.amazon\.com/vpc/](https://console.aws.amazon.com/vpc/)\.

1. On the navigation pane, choose **Transit Gateway Attachments**\.

1. Choose the search bar, select **Resource type** from the menu, and then select **VPN**\.

1. The VPN attachments are displayed\. Choose an attachment to view its details or to add tags\.

**To view your VPN attachments using the AWS CLI**  
Use the [describe\-transit\-gateway\-attachments](https://docs.aws.amazon.com/cli/latest/reference/ec2/describe-transit-gateway-attachments.html) command\.