# Bitcoin Exchange Rates in one bash command

```bash
curl_bitcoin=$(curl 'https://blockchain.info/fr/ticker' -s);echo "Bitcoin Exchange Rates / EUR: $(echo $curl_bitcoin | jq '.EUR.last')$(echo $curl_bitcoin | jq '.EUR.symbol' | cut -c 2-4) / USD: $(echo $curl_bitcoin | jq '.USD.last')$(echo $curl_bitcoin | jq '.USD.symbol' | cut -c 2)" && echo ""
```

Result:
```
Bitcoin Exchange Rates / EUR: 1994.63€ / USD: 2230.13$
```


Command to put in ~/.bashrc or /etc/.bashrc
