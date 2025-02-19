---
title: "tEVM Controller"
hide_table_of_contents: true
sidebar_position: 8
---


# <kbd>module</kbd> `tevmc`




**Global Variables**
---------------
- **DEFAULT_DOCKER_LABEL**
- **DEFAULT_FILTER**
- **MAX_STATUS_SIZE**


---


## <kbd>class</kbd> `TEVMCException`








---


## <kbd>class</kbd> `TEVMController`





### <kbd>method</kbd> `__init__`

```python
__init__(
    config: Dict[str, Dict],
    logger=None,
    log_level: str = 'info',
    root_pwd: Optional[Path] = None,
    wait: bool = False,
    services: List[str] = ['redis', 'elastic', 'kibana', 'nodeos', 'indexer', 'rpc', 'beats'],
    from_latest: bool = False,
    is_producer: bool = True,
    skip_init: bool = False
)
```








---


### <kbd>method</kbd> `await_full_index`

```python
await_full_index()
```





---


### <kbd>method</kbd> `darwin_network_setup`

```python
darwin_network_setup()
```





---


### <kbd>method</kbd> `must_keep_running`

```python
must_keep_running(container: str)
```





---


### <kbd>method</kbd> `open_container`

```python
open_container(name: str, image: str, *args, **kwargs)
```

Start a new container. 

Also waits for container to get ip address. 

---


### <kbd>method</kbd> `open_rpc_websocket`

```python
open_rpc_websocket()
```





---


### <kbd>method</kbd> `restart_translator`

```python
restart_translator()
```





---


### <kbd>method</kbd> `setup_index_patterns`

```python
setup_index_patterns(patterns: List[str])
```





---


### <kbd>method</kbd> `setup_rpc_log_mount`

```python
setup_rpc_log_mount()
```





---


### <kbd>method</kbd> `sigusr1_handler`

```python
sigusr1_handler(signum, frame)
```





---


### <kbd>method</kbd> `start`

```python
start()
```





---


### <kbd>method</kbd> `start_beats`

```python
start_beats()
```





---


### <kbd>method</kbd> `start_elasticsearch`

```python
start_elasticsearch()
```





---


### <kbd>method</kbd> `start_evm_rpc`

```python
start_evm_rpc()
```





---


### <kbd>method</kbd> `start_kibana`

```python
start_kibana()
```





---


### <kbd>method</kbd> `start_nodeos`

```python
start_nodeos(space_monitor=True, do_init=True)
```

Start eosio_nodeos container. 


- Initialize CLEOS wrapper and setup keosd & wallet. 
- Launch nodeos with config.ini 
- Wait for nodeos   to produce blocks 
- Create evm accounts and deploy contract 

---


### <kbd>method</kbd> `start_redis`

```python
start_redis()
```





---


### <kbd>method</kbd> `start_telosevm_translator`

```python
start_telosevm_translator()
```





---


### <kbd>method</kbd> `stop`

```python
stop()
```





---


### <kbd>method</kbd> `stop_elasticsearch`

```python
stop_elasticsearch()
```





---


### <kbd>method</kbd> `stream_logs`

```python
stream_logs(container, timeout=30.0, from_latest=False)
```








---

_This file was automatically generated via [lazydocs](https://github.com/ml-tooling/lazydocs)._
