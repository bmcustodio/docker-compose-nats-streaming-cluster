# docker-compose-nats-streaming-cluster

A three-node [NATS Streaming](https://github.com/nats-io/nats-streaming-server) cluster running on top of [Docker Compose](https://docs.docker.com/compose/) for testing purposes.

## Starting

To start the cluster, run

```
$ docker-compose up
(...)
nats-streaming-3_1  | [1] 2019/08/20 13:17:02.219196 [INF] STREAM: Starting nats-streaming-server[nats-streaming] version 0.16.0
(...)
nats-streaming-2_1  | [1] 2019/08/20 13:17:02.343457 [INF] STREAM: Starting nats-streaming-server[nats-streaming] version 0.16.0
(...)
nats-streaming-1_1  | [1] 2019/08/20 13:17:02.448176 [INF] STREAM: Starting nats-streaming-server[nats-streaming] version 0.16.0
(...)
```

## Connecting

To connect to the cluster, point your NATS Streaming client at one of `127.0.0.1:{14222,24222,34222}`:

## Stopping

To stop the cluster, hit `Ctrl+C`.

## Destroying

To desstroy the cluster, run

```
$ docker-compose down
Removing docker-compose-nats-streaming-cluster_nats-streaming-3_1 ... done
Removing docker-compose-nats-streaming-cluster_nats-streaming-2_1 ... done
Removing docker-compose-nats-streaming-cluster_nats-streaming-1_1 ... done
Removing network docker-compose-nats-streaming-cluster_main
```

## License

Copyright 2019 bmcstdio

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
