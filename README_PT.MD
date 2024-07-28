
# OVA para Desenvolvimento e Teste de Aplicações PHP com CodeIgniter 3.1.13

Esta OVA está configurada para facilitar o desenvolvimento e teste de aplicações PHP baseadas no framework CodeIgniter 3.1.13 em ambientes locais. A configuração é projetada para ser usada em um ambiente de desenvolvimento e não inclui configurações de VHOSTs, IPTables ou SSL para evitar complicações desnecessárias neste contexto.

## Características da OVA

- **Sistema Operacional:** Ubuntu 24.04 LTS
- **Servidor Web:** Apache 2.4.62
- **Linguagem de Programação:** PHP 8.3
- **Framework:** CodeIgniter 3.1.13
- **Banco de Dados:** MySQL 8.3.9
- **Acesso à Sessão, SSH e MySQL:**
  - **Usuário:** `devadmin`
  - **Senha:** `d3v4dm1n`

## Baixar, Acessar e Usar

Primeiro, é necessário baixar a OVA. Para fazer isso, clique no seguinte link:
[Desenvolvimento de Aplicações com CI 3.1.13.ova](https://mega.nz/file/5oJCEYja#M6ICl_uhYz6b5lHPucNpQq7NyWLixTW-Eh0pOLeUcxI)

Para usar esta OVA, você precisa importá-la no Virtualbox ou VMware e configurar a interface de rede como NAT ou outra opção. Uma vez que a VM esteja configurada e iniciada, você deve acessá-la com as credenciais de Sessão e, para obter o endereço IP da máquina, execute o comando

```bash
ip a
```

### SSH

Para acessar a máquina virtual via SSH, use as seguintes credenciais:

- **Usuário:** `devadmin`
- **Senha:** `d3v4dm1n`

```bash
ssh devadmin@<IP-da-OVA>
```

### MySQL

Para acessar o MySQL:

```bash
mysql -u devadmin -p
```

### Ambiente de Trabalho

O ambiente de trabalho está localizado no diretório `/var/www/html`, que é dividido em:

- `/var/www/html/sql`: para o gerenciador de banco de dados (PHPMyAdmin 5.2.1), acessível via URL: http://<IP-da-OVA>/sql/
- `/var/www/html/public`: para o CodeIgniter 3.1.13, acessível via URL: http://<IP-da-OVA>/public/

### Apache

O Apache está configurado para servir o projeto a partir do diretório `/var/www/html`. Não é necessário modificar as configurações de VHOST para o ambiente de desenvolvimento.

### PHP

A OVA inclui PHP 8.3 com as extensões necessárias para executar o CodeIgniter e outras aplicações web comuns. Se precisar instalar extensões adicionais, você pode fazê-lo usando `apt-get`.

```bash
sudo apt install php-<extension>
```

## Notas Adicionais

- Esta OVA está configurada para ambientes locais e não é recomendada para uso em produção.
- Para qualquer problema ou dúvida, entre em contato comigo.

## Licença

Esta OVA é fornecida tal como está, sem garantias de qualquer tipo. Use por sua própria conta e risco.
