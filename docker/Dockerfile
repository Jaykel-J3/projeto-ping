# Usar uma imagem base mínima
FROM alpine:latest
 
# Instalar o pacote 'iproute2' para permitir o uso de 'ip route'
RUN apk add --no-cache iproute2
 
# Comando padrão: ping contínuo no gateway padrão da rede
CMD ["sh", "-c", "ping $(ip route | awk '/default/ {print $3}')"]
