# spinup-redshift-cluster
Playbook to Spinup (Spin-Up) Redshift Cluster

### Architecture for Redshift Cluster:
* Virtual Private Cloud (VPC)
* Public subnets and private subnets
* Bastion host in public subnet, with SQL Client such as Aginity Workbench
* Redshift Cluster is in private subnet
* Security group of private subnet allows network traffice from public subnet (port 5349)


### References:
* AWS CloudFormation User Guide.  Redshift templates.  https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/sample-templates-services-us-west-2.html#w2ab1c35c58c13c31
  * Basic Redshift cluster.  https://s3.us-west-2.amazonaws.com/cloudformation-templates-us-west-2/Redshift.template
  * Redshift cluster in VPC.  https://s3.us-west-2.amazonaws.com/cloudformation-templates-us-west-2/RedshiftClusterInVpc.template
* AWS Blog.  Automate Amazon Redshift cluster creation using AWS CloudFormation.  https://aws.amazon.com/blogs/big-data/automate-amazon-redshift-cluster-creation-using-aws-cloudformation/
    * MainUsername
    * MainPassword
  * VPC CloudFormation Template.  https://aws-bigdata-blog.s3.amazonaws.com/artifacts/Automate_Redshift_Cluster_Creation_CloudFormation/aws-vpc-blog.template
  * Amazon Linux Bastion Host CloudFormation Template.  https://aws-bigdata-blog.s3.amazonaws.com/artifacts/Automate_Redshift_Cluster_Creation_CloudFormation/linux-bastion-blog.template
  * Amazon Redshift CloudFormation Template.  https://aws-bigdata-blog.s3.amazonaws.com/artifacts/Automate_Redshift_Cluster_Creation_CloudFormation/redshift-blog.template
* Shravan Kuchkula.  Create AWS Redshift cluster using AWS python SDK.  https://shravan-kuchkula.github.io/create-aws-redshift-cluster/#
* Shravan Kuchkula.  Project: Data Pipelines with Airflow.  https://github.com/shravan-kuchkula/Data-Pipelines-with-Apache-Airflow
* Shravan Kuchkula.  ETL data pipeline to process StreetEasy data.  https://github.com/shravan-kuchkula/Data-Pipeline-Batch-ETL-with-Airflow
* Pandas-Redshift library.  https://github.com/agawronski/pandas_redshift
