# 👋 Welcome to SSH + Printunl connection action

This action allow and turn more easy connect and run scripts in server using SSH and Printunl VPN

## ✅ Inputs

| Name          | Required      | Description                                   | Has Default Value?    |
|----------     |-------------  |--------------------------                     |--------               |
| `host`        | ✅            | Nome do usuário                               | ❌                    |
| `port`        | ✅            | port to server access                         | ✅ (22)               |
| `username`    | ✅            | login to server access                        | ❌                    |
| `private_key` | ✅            | private key to server access                  | ❌                    |
| `script`      | ❌            | script that you want to works on the server   | ❌                    |

## 🚀 Example

```yaml
- name: Connect SSH with Pritunl
  uses: anselmo-lopes/connect-ssh-printunl@v1
  with:
    host        : "127.0.0.1"
    username    : "root"
    port        : 23
    private_key : "yb39ub3fubrnr3on3r0ir0in3r...99fwf0e00q"
    script      : |
        echo "Hello World!"

```