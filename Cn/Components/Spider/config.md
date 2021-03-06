---
title: Spider
meta:
  - name: description
    content: EasySwoole-Spider 可以方便用户快速搭建分布式多协程爬虫。
  - name: keywords
    content: swoole|swoole 拓展|swoole 框架|easyswoole|spider|爬虫
---

## Config

设置生产端
```php
    public function setProduct(ProductInterface $product): Config
```

设置消费端
```php
    public function setConsume(ConsumeInterface $consume): Config
```

设置队列类型,Config::QUEUE_TYPE_FAST_CACHE、Config::QUEUE_TYPE_REDIS
```php
    public function setQueueType($queueType): Config
```

设置自定义队列,当组件中的队列方式不能满足您的需求时，可以自己实现队列
```php
    public function setQueue($queue): Config
```

分布式时指定某台机器为开始机
```php
    public function setMainHost($mainHost): Config
```

设置job-queue组件的队列key

```php
    public function setJobQueueKey($jobQueueKey): Config
```


设置自定义队列配置(现在只有redis-pool需要这个方法)

```php
    public function setJobQueueKey($jobQueueKey): Config
```

设置job-queue进程配置

```php
    public function setJobQueueProcessConfig(\EasySwoole\Component\Process\Config $config) : Config
```

设置最大协程数量(生产+消费总共)

```php
    public function setMaxCoroutineNum($maxCoroutineNum): Config
```