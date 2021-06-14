docker-compose up
docker exec client tc qdisc add dev eth0 root netem delay 100ms


ren@rennoMacBook-ea-2 rabit-play % docker exec l-rabit tc qdisc add dev eth0 root netem delay 100ms
ren@rennoMacBook-ea-2 rabit-play % docker exec client ping l-rabit
PING l-rabit (172.22.0.3) 56(84) bytes of data.
64 bytes from l-rabit.rabit-play_default (172.22.0.3): icmp_seq=1 ttl=64 time=210 ms
64 bytes from l-rabit.rabit-play_default (172.22.0.3): icmp_seq=2 ttl=64 time=102 ms
64 bytes from l-rabit.rabit-play_default (172.22.0.3): icmp_seq=3 ttl=64 time=100 ms
64 bytes from l-rabit.rabit-play_default (172.22.0.3): icmp_seq=4 ttl=64 time=102 ms
64 bytes from l-rabit.rabit-play_default (172.22.0.3): icmp_seq=5 ttl=64 time=100 ms
