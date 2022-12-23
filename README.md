# [(remote-ssh-commands-action)](https://github.com/Sithi5/remote-ssh-commands-action)

## How to use

```yml
uses: ./
    with:
        SSH_USER: ${{ secrets.SSH_USER }}
        SSH_PRIVATE_KEY: ${{ secrets.SSH_PRIVATE_KEY }}
        SSH_HOST: ${{ secrets.SSH_HOST }}
        SSH_REMOTE_COMMANDS: ls -la;pwd;echo "yeah"
```
