---
- name: Install HTTPD and VSFTPD on all hosts
  hosts: all
  become: true

  tasks:
    - name: Install httpd and vsftpd
      ansible.builtin.package:
        name:
          - httpd
          - vsftpd
        state: present

    - name: Enable and start httpd
      ansible.builtin.service:
        name: httpd
        state: started
        enabled: true

    - name: Enable and start vsftpd
      ansible.builtin.service:
        name: vsftpd
        state: started
        enabled: true
