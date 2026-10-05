# Docker Assignment 1

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

Result:

```text
Permission denied
```

## Conclusion

Both Part 1 and Part 2 of Docker Assignment 1 were successfully completed and tested.
