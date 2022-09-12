
# OBTENER BLOQUE GENESIS
```bash
curl --silent -X GET "http://127.0.0.1:5001/get_chain" | jq
curl --silent -X GET "http://127.0.0.1:5002/get_chain" | jq
curl --silent -X GET "http://127.0.0.1:5003/get_chain" | jq
```

# CONECTAR LOS NODOS PARA DESCENTRALIZR LA RED
```bash
curl --silent -X POST -H "Content-Type: application/json" -d '{"nodes":["http://127.0.0.1:5002", "http://127.0.0.1:5003"]}' "http://127.0.0.1:5001/connect_node" | jq
curl --silent -X POST -H "Content-Type: application/json" -d '{"nodes":["http://127.0.0.1:5001", "http://127.0.0.1:5003"]}' "http://127.0.0.1:5002/connect_node" | jq
curl --silent -X POST -H "Content-Type: application/json" -d '{"nodes":["http://127.0.0.1:5001", "http://127.0.0.1:5002"]}' "http://127.0.0.1:5003/connect_node" | jq
```

# MINAR UN BLOQUE
```bash
curl --silent -X GET "http://127.0.0.1:5001/mine_block" | jq
```

# VER CADENA 1
```bash
curl --silent -X GET "http://127.0.0.1:5001/get_chain" | jq
```

# VER OTRAS CADENAS
```bash
curl --silent -X GET "http://127.0.0.1:5002/get_chain" | jq
curl --silent -X GET "http://127.0.0.1:5003/get_chain" | jq
```

# PROTOCOLO DE CONCENSO
```bash
curl --silent -X GET "http://127.0.0.1:5002/replace_chain" | jq
curl --silent -X GET "http://127.0.0.1:5003/replace_chain" | jq
```

# TRANSACCION CRIPTOMONEDAS
```bash
curl --silent -X POST -H "Content-Type: application/json" -d '{"sender": "Eric","receiver":"Tu","amount":10}' "http://127.0.0.1:5001/add_transaction" | jq
```

# MINAR UN BLOQUE
```bash
curl --silent -X GET "http://127.0.0.1:5001/mine_block" | jq
```

# ACUTUALIZR LAS OTRAS CADENAS
```bash
curl --silent -X GET "http://127.0.0.1:5002/replace_chain" | jq
curl --silent -X GET "http://127.0.0.1:5003/replace_chain" | jq
```
