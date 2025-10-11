# Project 2 — Flask CRUD (Obfuscated Keys)

Minimal Flask app exposing CRUD for `/users` using **obfuscated request keys**.

## Clone & Open

```bash
git clone https://github.com/drewmayberry11/CSIS_3385_Fall_2025_Mayberry.git
cd CSIS_3385_Fall_2025_Mayberry/Project_2
```

*(Open the `Project_2` folder inside the cloned repo.)*

## Run

```bash
python3 app.py    # binds 0.0.0.0:5000
```

## Input Key Mapping

- `doggy` → `username`
- `zebra42` → `password`
- `kittycat` → `email`
- `rocketShip` → `age`

## Methods Used (Examples)

**GET**

```bash
curl http://localhost:5000/users
```

**POST**

```bash
curl -X POST http://localhost:5000/users \
  -H "Content-Type: application/json" \
  -d '{"doggy":"MojoJojo","zebra42":"MojosSecretPassword","kittycat":"mojojojo@gmail.com","rocketShip":21}'
```

**PUT**

```bash
curl -X PUT http://localhost:5000/users/1 \
  -H "Content-Type: application/json" \
  -d '{"doggy":"BigBossLadyHaley"}'
```

**DELETE**

```bash
curl -X DELETE http://localhost:5000/users/2
```

## Notes

- In-memory data (resets on server restart).
- New user IDs are generated; use `GET /users` to find the actual ID before `PUT`/`DELETE`.