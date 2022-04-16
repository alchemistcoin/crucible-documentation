# Our Endpoints

### Reward Program Staked USD Values

{% swagger method="get" path="/get-program-staked-usd" baseUrl="http://crucible.wtf/api" summary="" %}
{% swagger-description %}
This endpoint will return a JSON object of Reward Programs and the Total Staked Value in USD for each program.
{% endswagger-description %}

{% swagger-parameter in="query" name="network" required="true" %}
Network ID that data is required for



e.g:

1 = Mainnet

41334 = Avalanche
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Endpoint will return an array of reward programs and their total staked USD values" %}
```javascript
[{
    rewardProgramAddress, totalStakedUSD
}]
```
{% endswagger-response %}
{% endswagger %}

### Reward Program Reward USD Values

{% swagger method="get" path="/get-program-rewards-usd" baseUrl="http://crucible.wtf/api" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="network" %}
Network ID that data is required for



e.g:

1 = Mainnet

41334 = Avalanche
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Endpoint will return an array of reward programs and their total rewards (of all tokens within the pool) in USD values" %}
```javascript
[{
    rewardProgramAddress, totalRewardsUSD
}]
```
{% endswagger-response %}
{% endswagger %}
