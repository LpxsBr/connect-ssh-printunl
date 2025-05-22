# 👋 Welcome to SSH + Printunl connection action - V1.1

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
  uses: LpxsBr/connect-ssh-printunl@v1.1
  with:
    host                  : ${{ secrets.HOST                  }}
    username              : ${{ secrets.USERNAME              }}
    port                  : ${{ secrets.PORT                  }}
    private_key           : ${{ secrets.PRIVATE_KEY           }}
    printunl_profile_file : ${{ secrets.PRITUNL_PROFILE_FILE  }}
    printunl_profile_pin  : ${{ secrets.PRITUNL_PROFILE_PIN   }}
    script : |
        echo "Hello World!"
        cd project
        php artisan cache:clear

```


## Internal Actions

This actions internally use:

 - [nathanielvarona/pritunl-client-github-action@v1](https://github.com/nathanielvarona/pritunl-client-github-action)