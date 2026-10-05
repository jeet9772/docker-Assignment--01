<img width="1440" height="900" alt="Screenshot 2026-10-05 at 5 57 04 PM" src="https://github.com/user-attachments/assets/f2304628-06f0-4a02-9f21-7219b3b58cbf" /># Docker Assignment 1

## Part 1 – Static Website Using Docker

Created a Docker-based static website that displays different messages according to the time.

### Working Time

* **10 AM – 12 PM:** `10-12 | Hello from Jeetendra`
* **4 PM – 6 PM:** `4-6 | Hello from Vishu`

### Technologies Used

* Docker
* Python
* Flask

### Docker Commands

```bash
docker build -t jeetendra-time-site .
docker run -d --name jeetendra-time-website -p 8080:80 jeetendra-time-site
```

Test:

```bash
curl http://localhost:8080
```

<img width="1440" height="900" alt="Screenshot 2026-10-05 at 5 29 17 PM" src="https://github.com/user-attachments/assets/de87993e-2c67-4ab0-bb46-e5be81ed429b" />

---

## Part 2 – Docker User Permissions

Created the following directory structure:

```text
Data/
└── Ninjas/
    ├── Mohan/
    ├── Uma/
    ├── Shikha/
    └── Mayank/
```
<img width="1440" height="900" alt="Screenshot 2026-10-05 at 6 17 53 PM" src="https://github.com/user-attachments/assets/4c2eab2f-97ba-426b-97c9-68128e4bf3a4" />


The container runs as the `mohan` user.

### Permissions

* **Mohan:** Read + Write permission on `Mohan/`
* **Uma:** Read-only for Mohan
* **Shikha:** Read-only for Mohan
* **Mayank:** Read-only for Mohan

### Verification

Check current user:

```bash
whoami
```

<img width="1440" height="900" alt="Screenshot 2026-10-05 at 6 22 48 PM" src="https://github.com/user-attachments/assets/376e2682-2436-41ee-b73a-ab0e0293dccc" />

Output:

```text
mohan
```

Write test in Mohan directory:

```bash
touch /Data/Ninjas/Mohan/test.txt
```

Result: **Successful**

Write test in Uma directory:

```bash
touch /Data/Ninjas/Uma/test.txt
```

<img width="1440" height="900" alt="Screenshot 2026-10-05 at 5 57 04 PM" src="https://github.com/user-attachments/assets/bf1b9a57-cc1b-404b-94f3-c790869d8562" />

Result:

```text
Permission denied
```


## Conclusion

Both Part 1 and Part 2 of Docker Assignment 1 were successfully completed and tested.
