# Indexing, Selecting & Assigning

## Indexing
* 파이썬은 `iloc`와 `loc`두가지 방법이 있다.
* 두가지 방법모두 행이 우선된다.
* `:`이걸로 범위를 지정할수 있고, 리스트로도 범위를 지정할 수 있다.
* `.set_index("")`를 통하여 인덱스를 설정할수 있다.

1. Index-based selection `iloc`
  > index기반 선택으로 데이터의 숫자위치를 기반으로 접근한다.<br>
  > `파이썬과 같이 마지막 행을 포함하지 않느다.
2. Label-based selection `loc`
  > `위치보다 데이터 인덱스의 값이 더 중요하다. <br>
  > `마지막 행을 포함한다. 왜냐하면 값으로 접근하기 때문에 다음 값을 확인하기 어렵다.

## Selecting

1. Conditional selection
* 조건에 따라서 선택한다.
* `reviews.country == 'Italy'`로 접금하면 boolean값을 반환하고
* `reviews.loc[reviews.country == 'Italy']`로 접근하면 행을 반환해준다.
* &(어퍼센트)를 이용하여 조건을 결합 한다.
* |를 통하여 or을 사용한다.
* `isin()`을 사용하면 값 목록에 있는 데이터를 선택할 수 있습니다 `reviews.loc[reviews.country.isin(['Italy', 'France'])]`
* `isnull()`또는 `nounull()`을 이용하여 NaN값을 강조할수있다. `reviews.loc[reviews.price.notnull()]`

## Assigning
`reviews['critic'] = 'everyone'` 또는 `reviews['index_backwards'] = range(len(reviews), 0, -1)` 방벙이 있다.
