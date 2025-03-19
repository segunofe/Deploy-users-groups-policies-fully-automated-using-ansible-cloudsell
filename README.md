DEPLOYING USERS, GROUPS AND POLICIES IN A100% AUTOMATED WAY USING ANSIBLE AND CLOUD SHELL
![image](https://github.com/user-attachments/assets/e4302554-c13c-45b0-bc79-d7b71121dcf6)


You, as a Cloud Specialist, have the mission to create Users, Groups and Policies in the Oracle Cloud Infrastructure.

An easy task to accomplish using the console in the OCI, which is not a viable solution for large scale cases.
So, the goal will be to create these resources in an automated way using a powerful tool called Ansible! 

# Pre-reqs - Console OCI
Step 1: Create
- You should have the compartments below already in place: 
networkingResources
computeResources
databaseResources
![image](https://github.com/user-attachments/assets/2ac2eaa8-5942-4fd9-97ac-28e748b14e2c)

 

# Steps using the Cloud Shell in OCI
Step 2: Setting up the environment variable so that the ansible playbook can work since these variables were referred to inside the playbook. 

Get and replace the OCID of the Tenancy and the compartments:

NetworkingResources, ComputeResources and databaseResources:

export PARENT_COMPARTMENT_OCID=<insert-TENANCY-ocid>
export NETWORKING_COMPARTMENT_OCID=<insert-NETWORKING_COMPARTMENT-ocid>
export COMPUTE_COMPARTMENT_OCID=<insert-COMPUTE_COMPARTMENT-ocid>
export DB_COMPARTMENT_OCID=<insert-DB_COMPARTMENT-ocid>
![image](https://github.com/user-attachments/assets/afdc37d2-5157-4e57-a6d1-1e57c84f10d4)

 

Step 3: Creating and accessing a folder to download the code

mkdir tcb-bmc-iam
cd tcb-bmc-iam

Step 4: Downloading the file Ansible Playbooks

wget https://objectstorage.us-ashburn-1.oraclecloud.com/p/eRJ8pKclDBA_MZeuAqj75jkfPq3yvuqe4TslzNjqY7Y1RKTLMGipnbwfPO7cnp5F/n/idqfa2z2mift/b/bootcamp-oci/o/EN/oci-handson-module-iam.zip

unzip oci-handson-module-iam.zip
Step 5:
- Running the Ansible Playbooks from Cloud Shell

ansible-playbook tcb-bmc-iam-creating-groups-and-policies.yaml
 
 ![image](https://github.com/user-attachments/assets/431ed5db-8339-4326-82c6-c19875f632e1)
 ![image](https://github.com/user-attachments/assets/68509402-3818-4679-a6e3-d6039b45c944)
![image](https://github.com/user-attachments/assets/f5fddea0-0445-4dfc-b112-7b5fd04b1322)
![image](https://github.com/user-attachments/assets/a332a965-d104-427c-9177-977fbd7f25df)
![image](https://github.com/user-attachments/assets/65663f6d-c88d-4ccf-88c5-2ac9e6b30e50)




 
 
 
ansible-playbook tcb-bmc-iam-creating-users-cloud-admin.yaml
![image](https://github.com/user-attachments/assets/6bbe2e30-424f-4493-8d2e-262ffc6f2292)

![image](https://github.com/user-attachments/assets/3c8a9436-6115-4064-a318-2317a9a77df1)
 
 
ansible-playbook tcb-bmc-iam-creating-users-dba-admin.yaml
![image](https://github.com/user-attachments/assets/6669c8c6-69f7-4081-8991-b44e4d43b71a)
![image](https://github.com/user-attachments/assets/fcc27915-a2c7-4444-9ff2-8f47bc6a4109)


 
 
ansible-playbook tcb-bmc-iam-creating-users-network-admin.yaml
![image](https://github.com/user-attachments/assets/23b9e185-1935-4463-ba26-240b183b6ea7)

 
 
ansible-playbook tcb-bmc-iam-creating-users-compute-admin.yaml
 
 
ansible-playbook tcb-bmc-iam-creating-users-operators.yaml
![image](https://github.com/user-attachments/assets/79402d44-7ac0-4149-acbc-8758b22f77cd)
![image](https://github.com/user-attachments/assets/5c2dfcea-2410-4cdc-b216-c837afeae66b)
![image](https://github.com/user-attachments/assets/ad8240e9-24d9-4a5d-b496-e3d5478165f4)



 
  
 
 
 
 

