Deploy a virtual machine on VMware vSphere
==========================================

Requirements
------------

- Ansible >= 2.16.2
- community.vmware collection
- vmware_vm_manager role

How to use
----------

- Instal Ansible, from a package manager of your distribution or using python
    - For EL based use dnf
        1. Install Ansible rpm package
            ```
            dns install ansible
            ```            
    - From the pip
        1. Create a virtualenvironment
            ```
            python -m venv ansible
            ```
        2. Activate the venv created on the step 1
            ```
            source $PWD/ansible/bin/activate
            ```
        3. Install Ansible package:
            ```
            pip install -U ansible
            ```

- Installing Ansible collections and roles
    1. Installing Ansible collections from the requirements file
        ```
        ansible-galaxy collection install -r collections/requirements.yaml -p ./collections
        ```
    2. Installing Ansible roles from the requirements file
        ```
        ansible-galaxy role install -r collections/requirements.yaml -p ./collections
        ```

- Installing _community.vmware_ collection requirements
    ```
     pip install -U -r collections/ansible_collections/community/vmware/requirements.txt
    ```

- Run the playbook
    ```
    ansible-playbook playbook.yaml
    ```
License
-------

MIT License

Author Information
------------------

shellclear@gmail.com
