
1. $의 의미? cf : _의 의미?
```
_개인 인스턴스 속성용입니다.

Vue는 _ 접두사를 사용하여 자체 개인 속성을 정의합니다...

$공용 인스턴스 속성용입니다.

$ 접두사의 경우 Vue 생태계 내에서의 목적은 사용자에게 노출되는 특수 인스턴스 속성입니다

```
- $접두사는 Vue의 핵심 API에서만 사용되는 것이 아닙니다.
- 구성 요소에 속성을 추가하는 라이브러리에서도 일반적으로 사용됩니다.
```
예:

Vuex는 $store.
Vue 라우터는 $route및 $router.
```

2. store에서 mapActions
```
..mapActions([
  'increment' // this.increment()을 this.$store.dispatch('increment')에 매핑
]),
...mapActions({
  add: 'increment' // this.add()을 this.$store.dispatch('increment')에 매핑
})
```

3. watch
- watch 속성은 특정 데이터의 변화를 감지하여 자동으로 특정 로직을 수행해주는 속성

4. computed
- 컴퓨티드(computed) 속성은 템플릿의 데이터 표현을 더 직관적이고 간결하게 도와주는 속성