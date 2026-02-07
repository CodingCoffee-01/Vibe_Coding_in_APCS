以下是 C 語言中輸入與輸出的教學，包含程式碼範例與說明，並以 Markdown 格式呈現：

---

# C 語言 Input/Output 教學

在 C 語言中，輸入與輸出是程式與使用者互動的基本功能。以下介紹常用的輸入與輸出函式，並提供範例程式碼。

---

## 1. 輸出 (Output)

C 語言中最常用的輸出函式是 `printf`，它用於將資料輸出到螢幕。

### 範例程式碼

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\\n"); // 輸出字串
    printf("整數: %d\\n", 42);   // 輸出整數
    printf("浮點數: %.2f\\n", 3.14); // 輸出浮點數，保留兩位小數
    return 0;
}
```

### 說明

- `printf` 是格式化輸出函式。
- 常見的格式化符號：
  - `%d`：整數
  - `%f`：浮點數
  - `%c`：單一字元
  - `%s`：字串
- `\\n`：換行符號，表示輸出後換行。

---

## 2. 輸入 (Input)

C 語言中最常用的輸入函式是 `scanf`，它用於從使用者那裡讀取資料。

### 範例程式碼

```c
#include <stdio.h>

int main() {
    int age;
    float height;
    char name[50];

    printf("請輸入您的名字: ");
    scanf("%s", name); // 讀取字串

    printf("請輸入您的年齡: ");
    scanf("%d", &age); // 讀取整數

    printf("請輸入您的身高 (cm): ");
    scanf("%f", &height); // 讀取浮點數

    printf("\\n輸入的資料如下:\\n");
    printf("名字: %s\\n", name);
    printf("年齡: %d\\n", age);
    printf("身高: %.2f cm\\n", height);

    return 0;
}
```

### 說明

- `scanf` 是格式化輸入函式。
- 常見的格式化符號與 `printf` 相同。
- 使用 `&` 符號來傳遞變數的記憶體位址（字串除外）。

---

## 3. 注意事項

1. **字串輸入的限制**：
   - `scanf("%s", name)` 只能讀取不含空格的字串。
   - 若需要讀取包含空格的字串，請使用 `fgets` 函式。

2. **輸入緩衝區問題**：
   - 使用 `scanf` 時，可能會因為換行符號留在緩衝區中導致問題。
   - 解決方法：在需要時使用 `getchar()` 清除緩衝區。

---

## 4. 綜合範例

以下是一個綜合範例，展示如何使用輸入與輸出函式：

```c
#include <stdio.h>

int main() {
    char name[50];
    int age;
    float score;

    printf("請輸入您的名字: ");
    scanf("%s", name);

    printf("請輸入您的年齡: ");
    scanf("%d", &age);

    printf("請輸入您的考試分數: ");
    scanf("%f", &score);

    printf("\\n--- 輸出結果 ---\\n");
    printf("名字: %s\\n", name);
    printf("年齡: %d\\n", age);
    printf("考試分數: %.2f\\n", score);

    return 0;
}
```

### 範例輸出

```
請輸入您的名字: Alice
請輸入您的年齡: 20
請輸入您的考試分數: 95.5

--- 輸出結果 ---
名字: Alice
年齡: 20
考試分數: 95.50
```

---

希望這份教學對您學習 C 語言的輸入與輸出有所幫助！
