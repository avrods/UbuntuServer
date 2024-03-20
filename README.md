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
```bash
sudo nano /etc/nginx/sites-available/AQUICAMBIAR.conf
```
