# Open Search

Projeto de exemplo do Open Search usando docker compose na máquina local,
seguindo o [quickstart](https://opensearch.org/docs/latest/quickstart) da documentação.

# Configuração

```
# Disable memory paging and swapping.
sudo swapoff -a

# Edit the sysctl config file that defines the host's max map count.
sudo vi /etc/sysctl.conf

# Set max map count to the recommended value of 262144.
vm.max_map_count=262144

# Reload the kernel parameters.
sudo sysctl -p
```

# Començar

Subir o projeto:

```console
make up
```

Teste se está funcionando:

```console
curl https://localhost:9200 -ku admin:admin
```

Acesse o dashboard pelo endereço http://localhost:5601
usando usuário `admin` e senha `admin`.
