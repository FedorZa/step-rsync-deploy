# RSync deployment step
Deploy your code to any server over ssh using rsync. By default it will upload the whole directory to the target.
use Env variables for setup target path!

[![wercker status](https://app.wercker.com/status/9d72a4b411b0c34231e71fbac8c989e3/m "wercker status")](https://app.wercker.com/project/bykey/9d72a4b411b0c34231e71fbac8c989e3)

# Options

* `host` the hostname to connect to
* `directory` the remote directory to upload to
* `sshkey` the private key file to use for authentication
* `user` (optional) the username used for the connection, default is `ubuntu`
* `sshport` (optional) the port that ssh uses for the connection, default is `22`
* `source` (optional) specify which source directory to upload, default is `./`
* `group` (optional) specify which group should be applied via chown user:

# Example

    - fedor/rsync-soft-deploy@0.1.40:
        host: example.org
        directory: /var/www
        sshkey: $PRIVATEKEY_FILE
		group: www-data