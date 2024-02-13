# Ehy Elemento give me a VM

# Aim of the hackaton

Develop something (script, npm module, python package, docker container, C++ executable) able to call an API and made a request

# Track

## AI track

- train a model to create new mesOS translators
- train a model to create [custom configs](https://github.com/Elemento-Modular-Cloud/electros)
- train a model to infer configs from Software specs found on the internet

## Presentation
![Elemento_page-0003](https://github.com/Paolo-Beci/NASA-Space-Apps-2023/assets/71789321/d8ca3235-a016-4864-a5c0-7d91c4b3020e)
![Elemento_page-0004](https://github.com/Paolo-Beci/NASA-Space-Apps-2023/assets/71789321/81d3c55b-ad28-448d-8c9d-9c5872ded70c)
![Elemento_page-0005](https://github.com/Paolo-Beci/NASA-Space-Apps-2023/assets/71789321/04d1dcb5-6b82-4537-80d9-72de4ede80ba)
![Elemento_page-0006](https://github.com/Paolo-Beci/NASA-Space-Apps-2023/assets/71789321/a0a55f09-ed98-4081-9598-ea3a15d4a199)

## API

here the calls the should be reproduced by your code. `localhost` is the location of the machine running daemons

### Register
#### GET /api/v1.0/client/vm/status
```
GET /api/v1.0/client/vm/status HTTP/1.1
Host: localhost:17777
Accept: application/json
```

#### POST /api/v1.0/client/vm/register
```
POST /api/v1.0/client/vm/register HTTP/1.1
Host: localhost:17777
Accept: application/json

{
  "vm_name": "VM",
  "slots": 2,
  "overprovision": 2,
  "allowSMT": false,
  "archs": ["X86_64"],
  "flags": ["sse2"],
  "ramsize": 2048,
  "reqECC": false,
  "misc": {"os_family": "windows", "os_flavour": "windows10"},
  "pci": [
      {
          "vendor": "10de",
          "model": "24b0",
          "quantity": 1
      },
      {
          "vendor": "10de",
          "model": "228b",
          "quantity": 1
      }
  ],
  "volumes":[],
  "netdevs": []
}
```

#### POST /api/v1.0/client/vm/unregister
```
POST /api/v1.0/client/vm/unregister HTTP/1.1
Host: localhost:17777
Accept: application/json

{
  "local_index": "ffffffff-fffff-ffff-ffff-ffffffffffff"
}
```

# Deliver
Commmit your code to [Elemento-Modular-Cloud/hackathon2023](https://github.com/Elemento-Modular-Cloud/hackathon2023)

# License
The code developed in this hackaton belongs to Elemento s.r.l. add your name in the license for a correct acknoledgment of your work

# Help
Do you need help? [Open an issue on us](https://github.com/Elemento-Modular-Cloud/helpcenter)
