# !/usr/bin/env python
# coding:utf-8

import platform
from smb.SMBConnection import SMBConnection

if __name__ == "__main__":

    # connection open
    conn = SMBConnection(
        'username',
        'password',
        platform.uname().node,
        'hostname',
        domain='',
        use_ntlm_v2=True)
    conn.connect('ipaddress', 139)

    items = conn.listPath('c$', 'target_folder')
    print([item.filename for item in items])

    conn.close()
