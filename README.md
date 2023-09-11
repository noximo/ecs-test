# ecs-test

ECS fails when working without cache.

How to reproduce:

Run command

> ./vendor/bin ecs check src --clear-cache

or

> composer ecs

Running commands 

> ./vendor/bin ecs check src

or

> composer ecs2

is successful


To mitigate the issue, paralelization needs to be turned off:

> $parameters = $ecsConfig->parameters();
> $parameters->set(Option::PARALLEL, false);
