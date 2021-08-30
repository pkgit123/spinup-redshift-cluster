# spinup-redshift-cluster
Playbook to Spinup (Spin-Up) Redshift Cluster

### Architecture for Redshift Cluster:
* Virtual Private Cloud (VPC)
* Public subnets and private subnets
* Bastion host in public subnet, with SQL Client such as Aginity Workbench
* Redshift Cluster is in private subnet
* Security group of private subnet allows network traffice from public subnet (port 5349)

### Notes:
* Warning: Redshift is a relatively expensive service, so be aware that it will incur charges to uptime, even if not using.
* Redshift has single-node vs. multi-node.  For prototyping purposes, the single-node cluster will be cheaper.
* Redshift has different node types.  Some node types have a minimum number of nodes.  Some node types combine storage and compute; other node types separate storage and compute.  The newer RA3 node type has 2-3 node minimum, but the advantage when scaling is that it separates compute from storage.
* Many AWS accounts have EC2 node maximum limits.  Be aware that creating a Redshift cluster may exceed the AWS account maximium limits, and will require special request to AWS Support.

### References:
* AWS CloudFormation User Guide.  Redshift templates.  https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/sample-templates-services-us-west-2.html#w2ab1c35c58c13c31
  * Basic Redshift cluster.  https://s3.us-west-2.amazonaws.com/cloudformation-templates-us-west-2/Redshift.template
  * Redshift cluster in VPC.  https://s3.us-west-2.amazonaws.com/cloudformation-templates-us-west-2/RedshiftClusterInVpc.template
* AWS Blog.  Automate Amazon Redshift cluster creation using AWS CloudFormation.  https://aws.amazon.com/blogs/big-data/automate-amazon-redshift-cluster-creation-using-aws-cloudformation/
    * MainUsername
    * MainPassword - can only contain letters and number (no special symbols)
  * VPC CloudFormation Template.  https://aws-bigdata-blog.s3.amazonaws.com/artifacts/Automate_Redshift_Cluster_Creation_CloudFormation/aws-vpc-blog.template
  * Amazon Linux Bastion Host CloudFormation Template.  https://aws-bigdata-blog.s3.amazonaws.com/artifacts/Automate_Redshift_Cluster_Creation_CloudFormation/linux-bastion-blog.template
  * Amazon Redshift CloudFormation Template.  https://aws-bigdata-blog.s3.amazonaws.com/artifacts/Automate_Redshift_Cluster_Creation_CloudFormation/redshift-blog.template
* Shravan Kuchkula.  Create AWS Redshift cluster using AWS python SDK.  https://shravan-kuchkula.github.io/create-aws-redshift-cluster/#
* Shravan Kuchkula.  Project: Data Pipelines with Airflow.  https://github.com/shravan-kuchkula/Data-Pipelines-with-Apache-Airflow
* Shravan Kuchkula.  ETL data pipeline to process StreetEasy data.  https://github.com/shravan-kuchkula/Data-Pipeline-Batch-ETL-with-Airflow
* Pandas-Redshift library.  https://github.com/agawronski/pandas_redshift
