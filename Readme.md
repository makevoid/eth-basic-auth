# eth-basic-auth

Ethereum Geth node setup behind nginx basic auth

---

Versions:

- Geth 1.9.3

(for Parity check the `geth` branch)


### Run

    docker-compose up --build


### Test it out

regenerate the .htpasswd (`htpasswd -c ./auth/.htpasswd geth`)

then run:

    geth attach http://geth:PASSWORD@localhost


### Regenerate the geth private key

Important, regenerate the private key, as this one is public domain :)

- regenerate the ethereum key via `geth account new`
- drop the key into `./eth/keys`

---

Enjoy!

@makevoid
