# ipfs-cluster
IPFS cluster setup

* [ipfs-cluster](https://github.com/ipfs/ipfs-cluster)


# Requirements
* Docker

# Commands 

* Ensure that following data is removed.
/cluster/peer1/config/ipfs-cluster-data 
/cluster/peer1/config/ipfs-cluster-data
* Only service.json will be present in  /cluster/[peer]/config
* Add  same secret for both peers in service.json
  ```json
  "secret": "6b4b8e2c88661341b243c865de64f4722cb613b38bab9b962820b42c175b9b3a",
  ```  
  
* Ensure peers is empty in service.json
  ```json
  "peers": [],
  ```

```bash
docker-compose -f docker-compose-ipfs-cluster.yaml up

//connect peer1 to peer2
docker exec ipfs_peer-1_1 ipfs-cluster-ctl peers add /ip4/172.20.0.2/tcp/9096/ipfs/QmbuWdsRWhasARr9Tm8aoAESahcHPEqYN1gT28Us2Jdssx
```


