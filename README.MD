# Gerar chave privada RSA256

`shell
openssl genpkey -algorithm RSA -out private_key.pem  -pkeyopt rsa_keygen_bits:2048
`

# Gerar chave publica

`shell
openssl rsa -pubout -in private_key.pem -out public_key.pem
`

# Converter para base64

`shell
base64 -i -w 0 private_key.pem > private_key-base64.txt
`