# Gradle

## Dependencies

- 프로젝트 의존성들은 관리의 용이성을 위해 분리 및 그룹화하여 관리한다.
- 라이브러리 추가 시, `buildSrc` 내의 `Versions` / `Dependencies` 에 분리해 명시한다.
- `Versions` - 라이브러리의 정확한 버전 명시
- `Dependencies` - 각 의존성을 그룹화하여 지정

```kotlin
// Versions.kt
object Versions {
  object Architecture {
    const val Lifecycle = "2.4.0"
  }
}
```

```kotlin
// Dependencies.kt
object Dependencies {
  val SharedKtx = listOf(
    "androidx.lifecycle:lifecycle-runtime-ktx:${Versions.Architecture.Lifecycle}"
  )
}
```

```kotlin
// build.gradle.kts
Dependencies.SharedKtx.forEach(::implementation)
```

