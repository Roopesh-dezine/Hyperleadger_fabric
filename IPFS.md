What is IPFS?

IPFS (InterPlanetary File System) is a peer-to-peer distributed file storage system. It allows users to store and share files in a decentralized way, using content-based addressing instead of location-based URLs.
Key Features:
->Files are identified by cryptographic hashes.
->Supports versioning and offline-first design.
->Efficient bandwidth usage via deduplication.
->Nodes store and cache files they access.

Step by Step implementation of Commands.....
1. Install the IPFS through WSL: wget https://dist.ipfs.tech/kubo/v0.32.1/kubo_v0.32.1_linux-amd64.tar.gz
2. tar -xvzf kubo_v0.32.1_linux-amd64.tar.gz
3. Kubo is a reference implementation of IPFS in Go: cd kubo
4. ls
5. sudo bash install.sh
6. ipfs –version
7. ipfs init

![Screenshot 2025-05-18 190139](https://github.com/user-attachments/assets/4db60398-6b37-49b2-8371-ec0d373692ee)

8.ipfs daemon

![Screenshot 2025-05-18 190243](https://github.com/user-attachments/assets/fcf37d50-9441-4b37-9eda-9b090b51bc66)

9. On Browser: http://127.0.0.1:5001/webui

![Screenshot 2025-05-18 211010](https://github.com/user-attachments/assets/2290bcf9-94d6-41fe-8d29-912dd78efe6f)

10. To run ipfs daemon in background: ipfs daemon > ipfs.log 2>&1 &
11. This is daemon ID: [1] 599
12. Add file: echo "Hello, IPFS!" > hello.txt
13. ipfs add hello.txt

![Screenshot 2025-05-18 210739](https://github.com/user-attachments/assets/edba5383-ad0f-43c7-a04d-d9b39e3f4b8b)

14. ipfs cat <CID>
15. Add a directory: mkdir myfolder
echo "File 1 content" > myfolder/file1.txt
echo "File 2 content" > myfolder/file2.txt
16. ipfs add -r myfolder
17. ps aux | grep ipfs
18. kill <PID>

![Screenshot 2025-05-18 210739](https://github.com/user-attachments/assets/f3ea2e5c-0691-4158-bf61-8c50a71c3dcd)

19. In Browser you can directly run this to see the IPFS: https://ipfs.io/ipfs/QmWd9cavD8UGZQcqYBVhZqs2Jure5W9cgxR7S6TC4StfZe

![Screenshot 2025-05-18 210956](https://github.com/user-attachments/assets/41af31de-0016-4e95-9f97-25bc3a74e560)
