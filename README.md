# pNFS community in Kubernetes

Running [pNFS community](https://github.com/kofemann/pnfs-community) in kubernetes.

## Requirements

- Access to kubernetes cluster (local or remote).
- `kubectl` binary

## The starting order

1. hazelcast

    ```
    $ kubectl apply -f hazelcast.yaml
    ```

1. zookeeper

    ```
    $ kubectl apply -f zookeeper.yaml
    ```

1. pNFS MDS config and server

    ```
    $ kubectl apply -f nfs-config.yaml
    $ kubectl apply -f nfs-mds.yaml
    ```
1. pNFS data servers

    ```
    $ kubectl apply -f nfs-ds.yaml
    ```

## Knows issues

The current hazelcast setup can have only a single node

## LICENSE

This work is published under [public domain](https://creativecommons.org/licenses/publicdomain/) license.
