# ipfs-cluster
IPFS cluster setup

* [ipfs-cluster](https://github.com/ipfs/ipfs-cluster)


# Requirements
* Docker

# Commands 

```bash
docker-compose -f docker-compose-ipfs-cluster.yaml up

docker exec ipfs_peer-1_1 ipfs-cluster-ctl peers add /ip4/172.20.0.2/tcp/9096/ipfs/QmbuWdsRWhasARr9Tm8aoAESahcHPEqYN1gT28Us2Jdssx

```


