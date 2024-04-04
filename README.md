# Snapshotter

Tool for creating data snapshots from remote Ethereum nodes, managed by EthPandaOps. 

## Usage

Snapshotter connects to a remote node over ssh and uses rclone to create a snapshot of client database data. 

Modify `config.example.yaml` to match your enviroment and connection to the node. 

Compile snapshotter with `go 1.21.6` or higher: 

```
go build -o snapshotter ./cmd/snapshotter
./snapshotter --config config.yaml
```
Or with Docker using provided Dockerfile:

```
docker build -t snapshotter .
```

