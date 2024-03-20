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
sudo rm -rf /etc/nginx/sites-enabled/defaut
```
```bash
sudo ln -s /etc/nginx/sites-available/AQUICAMBIAR.conf /etc/nginx/sites-enabled/
```
### Agregar configuración.

```bash
sudo nano /etc/nginx/sites-available/AQUICAMBIAR.conf
```

### Code Server.

```bash
curl -fsSL https://code-server.dev/install.sh | sh
```

Abrir este link: [Release Code](https://github.com/coder/code-server/releases)

```bash
wget https://github.com/coder/code-server/releases/download/v4.xx/xx_amd64.deb
```
```bash
sudo apt install ./code-server_*_amd64.deb
```
```bash
sudo systemctl start code-server@$USER
```
```bash
sudo systemctl enable --now code-server@$USER
```
```bash
sudo nano /etc/nginx/sites-available/AQUICAMBIAR.conf
```
```bash
server {
  listen 80;
  listen [::]:80;

  server_name yourdomain.com;
  #server_name system-ip-addres;

  location / {
    proxy_pass http://localhost:8080/;
    proxy_set_header Host $host;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection upgrade;
    proxy_set_header Accept-Encoding gzip;
  }
}
```
