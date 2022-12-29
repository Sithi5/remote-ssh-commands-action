# [(remote-ssh-commands-action)](https://github.com/Sithi5/remote-ssh-commands-action)

Execute command in a remote server with ssh private key.

## How to use

Put your secrets in your github secret repository, and add your bash commands separated with a `;`.

```yml
uses: Sithi5/remote-ssh-commands-action@main
    with:
        SSH_USER: ${{ secrets.SSH_USER }}
        SSH_PRIVATE_KEY: ${{ secrets.SSH_PRIVATE_KEY }}
        SSH_HOST: ${{ secrets.SSH_HOST }}
        SSH_PORT: 22
        SSH_REMOTE_COMMANDS: ls -la;pwd;echo "Hello World !"
```

An `exit` command is added by default after executing all inputs commands to close the ssh connection.

## Input variables

- `SSH_USER` - Required, ssh user
- `SSH_PRIVATE_KEY` - Required, ssh private key
- `SSH_HOST` - Required, ssh host address
- `SSH_PORT` - Optional, default to 22, ssh port
- `SSH_REMOTE_COMMANDS` - Bash commands to execute in the remote server. For multiple commands, separate them with `;`
