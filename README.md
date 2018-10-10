# myHelloSmartContract

Test with test net:

* alias cle="cleos  --url https://jungle.eosio.cr:443"

* push data to table of owner

** cle push action tamtamtamtam writemessage '{"username":"tamtamtamtam","msg":"Account Tam push data to table"}' -p tamtamtamtam
(tamtamtamtam is owner, add username"tamtamtamtam" to table with msg"Account Tam push data to table")
Result:

{
  "rows": [{
      "owner": "tamtamtamtam",
      "message": "Account Tam push data to table"
    }
  ],
  "more": false
}

** cle push action tamtamtamtam writemessage '{"username":"demdemdemdem","msg":"Account dem push data to table"}' -p demdemdemdem
(tamtamtamtam is owner, add username"demdemdemdem" to table with msg"Account Tam push data to table")
Result:
{
  "rows": [{
      "owner": "demdemdemdem",
      "message": "Account dem push data to table"
    },{
      "owner": "tamtamtamtam",
      "message": "Account Tam push data to table"
    }
  ],
  "more": false
}

*delete from table:
** cle push action tamtamtamtam rmmessage '{"username":"demdemdemdem"}' -p demdemdemdem
** cle push action tamtamtamtam rmmessage '{"username":"tamtamtamtam"}' -p tamtamtamtam

