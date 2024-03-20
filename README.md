### UbuntuServer 22.04
Gary Avendaño Rosado.

Al crear ya la maquina virtual esta es mi configuración:

```bash
sudo nano /etc/hostname
```
```bash
sudo nano /etc/hosts
```
```bash
sudo systemctl reboot
```

### Al reiniciar.

```bash
sudo apt install -y nginx
```
```bash
sudo snap install certbot --classic
```
```bash
sudo mv /etc/nginx/sites-available/AQUICAMBIAR.conf
```
```bash
sudo rm -rf /etc/nginx/sites-enable/defaut
```
```bash
sudo ln -s /etc/nginx/sites-available/AQUICAMBIAR.conf /etc/nginx/sites-enable/
```
### Agregar configuración.

```bash
sudo nano /etc/nginx/sites-available/AQUICAMBIAR.conf
```

### Code Server.

```bash
curl -fsSL https://code-server.dev/install.sh | sh
```

[Release Code](https://github.com/coder/code-server/releases)

```bash
wget https://github.com/coder/code-server/releases/download/v4.xx/xx_amd64.deb
```
