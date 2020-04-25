# eth-basic-auth

Ethereum node setup behind nginx basic auth

---

Versions:

- Parity 2.7


### Run

    docker-compose up --build


### Test it out

regenerate the .htpasswd (`htpasswd -c ./auth/.htpasswd parity`)

then run:

    geth attach http://parity:password@localhost


### Regenerate the parity private key

- regenerate the ethereum key via `parity account create`
- update the dockerfile

<!--
### Deploy it

- run deploy.rb (soon)  -->

---

Enjoy!

@makevoid
