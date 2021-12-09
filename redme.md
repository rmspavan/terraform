welcome to terraform...!

it is for infrastructure provides
    - configure that infrastructure
    - deploy apps
    - install/update software
    - create infra
    - changes to infrastructure
    - Automate the continuous chnages to your infra..
    - replicating infra.
    -
    $ cat aix_oslevel_check.yml
---

- name: AIX oslevel checking playbook 
  hosts: all 
  tasks:

  - name: Gather LPP Facts 
    shell: "oslevel -s"
    register: output_oslevel

  - name: Print the oslevel
    debug:
      msg: "{{ ansible_hostname }} has the AIX oslevel of {{ output_oslevel.stdout }}"

      https://www.ansible.com/blog/aix-patch-management-with-ansible