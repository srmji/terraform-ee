| OS Distribution        | Enterprise Engine           | UCP  | DTR |
| ------------- |:-------------:| -----:| -----:|
| RHEL 7.3      | See footnotes  | Any | Any |
| RHEL 7.4      | See footnotes      |   Any | Any |
| RHEL 7.5 | See footnotes      |    Any | Any |
| Windows Server 2016 | See footnotes      |    Any | Any |
| Windows Server 1709 | See footnotes      |    Any | Any |
| Windows Server 1803 | See footnotes      |    Any | Any |


# Background

You define your desired Docker EE cluster environment topology (nr of managers, workers) along 
with the desired software versions of different components (Host OS, Engine Release, UCP Release, DTR Release),
using a set of variables.


```
variables = {
    'os_version': "RHEL-7.5",
    'ee_version': "17.06.2-ee-14",
    'ucp_version': "3.0.2",
    'dtr_version': "2.5.3",
    'manager_count': 1,
    'dtr_count': 0,
    'linux_worker_count': 0,
    "windows_os_version": "2016_base",
    'windows_worker_count': 3,
}
```

```
python install.py
```

# Getting Started
 
```

1. Install terraform
2. Create a folder named files in the project directory.
2. Edit secret.tfvars as the example file, to set AWS credentials.
2. Run terraform init
3. Edit the variables in install.py
4. Run terraform apply with python install.py

```

# Example 1.

The example below will provision 4 node cluster consisting of 1 Manager 3 Worker nodes.

The manager will be hosted on a RHEL 7.5 machine with the Docker EE Engine 17.06.2-ee-14 release.
The worker nodes will be hosted on Windows Server 2016 with the same EE engine version as the linux one.

```
variables = {
    'os_version': "RHEL-7.5",
    'ee_version': "17.06.2-ee-14",
    'ucp_version': "3.0.2",
    'dtr_version': "2.5.3",
    'manager_count': 1,
    'dtr_count': 0,
    'linux_worker_count': 0,
    "windows_os_version": "2016_base",
    'windows_worker_count': 3,
}
```

# Example 2.

| First Header  | Second Header | Third Header | Third Header | 
| ------------- | ------------- | ------------ | ------------ | 
| Content Cell  | Content Cell  | Content Cell | Content Cell |       
| Content Cell  | Content Cell  | Content Cell | Content Cell | 

| OS  | Enterprise Engine | UCP | DTR |
| ------------- | ------------- | 
| RHEL 7.5 | *  | * | 
| RHEL 7.4 | *  | * |  
| RHEL 7.3 | *  | * | 

