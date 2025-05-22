# 👋 Welcome to SSH + Printunl connection action

This action allow and turn more easy connect and run scripts in server using SSH and Printunl VPN

## ✅ Inputs

| Name                    | Required      | Description                                   | Has Default Value?    |
|----------               |-------------  |--------------------------                     |--------               |
| `host`                  | ✅            | Nome do usuário                               | ❌                    |
| `port`                  | ❌            | port to server access                         | ✅ (22)               |
| `username`              | ✅            | login to server access                        | ❌                    |
| `private_key`           | ✅            | private key to server access                  | ❌                    |
| `printunl_profile_file` | ✅            | Base64 encoded Printunl File                  | ❌                    |
| `printunl_profile_pin`  | ✅            | Pin of Prinunl File                           | ❌                    |
| `script`                | ❌            | script that you want to works on the server   | ❌                    |

## 🚀 Example

```yaml
- name: Connect SSH with Pritunl
  uses: anselmo-lopes/connect-ssh-printunl@v1
  with:
    host        : ${{ secrets.HOST        }}
    username    : ${{ secrets.USERNAME    }}
    port        : ${{ secrets.PORT        }}
    private_key : ${{ secrets.PRIVATE_KEY }}
    script      : |
        echo "Hello World!"

```


## Internal Actions

This actions internally use:

 - [nathanielvarona/pritunl-client-github-action@v1](https://github.com/nathanielvarona/pritunl-client-github-action)