# Kotlin

## Code Rules

### Function vs Property

- 행동 또는 특정 액션에 대한 개념일 경우 Function

```kotlin
fun save()
fun load()
```

- 상태 및 정보를 가져오는 개념일 경우 Property(`Custom Accessor`)

```kotlin
val bearer
	get() = "Bearer $token"
```

> [Medium / Kotlin: should I define Function or Property?](https://blog.kotlin-academy.com/kotlin-should-i-define-function-or-property-6786951da909)