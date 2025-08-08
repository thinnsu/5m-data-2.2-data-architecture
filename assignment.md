# Assignment

## Brief

Write the Python codes for the following questions.

## Instructions

Paste the answer as Python in the answer code section below each question.

### Question 1

Question: How would you create a new hash in Redis to store information about a person, with `john_doe` as the key and include the name (`John Doe`), age (`35`), and email address (`john@email.com`)?

```python
import redis

r = redis.Redis(
  host='redis-10908.c252.ap-southeast-1-1.ec2.cloud.redislabs.com',
  port=10908,
  password='EgIvxgDuiuk2Sh5VnJzUGXDMtLrtK5Hk')
```

Answer:

```python
r.hset(
    'TutorialQ1',
    mapping={
        "age": 35,
        "email": "john@gmail.com",
        "name": "John Doe",
    },
```

### Question 2

Question: Write Python code to list the first 10 objects (blob name) in the "gcp-public-data-landsat" bucket, along with their sizes.

```python
from google.cloud import storage

client = storage.Client()
bucket = client.get_bucket("gcp-public-data-landsat")
```

Answer:

```python
# List the first 10 blobs in the bucket along with their sizes
blobs = bucket.list_blobs()

print("First 10 blobs in the bucket:")
for ix, blob in enumerate(blobs):
    print(f"Blob Name: {blob.name}")
    if ix == 9:  # Stop after listing 10 blobs
        break
```

## Submission

- Submit the URL of the GitHub Repository that contains your work to NTU black board.
- Should you reference the work of your classmate(s) or online resources, give them credit by adding either the name of your classmate or URL.
