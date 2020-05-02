# eth-basic-auth

Private fork of https://github.com/makevoid/eth-basic-auth but with an unknown private key :D

Ethereum node setup behind nginx basic auth

---

Versions:

- Geth 1.9.3

(for Parity check the `parity` branch)


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
