📝 بحث حول دوال المصفوفات ودوال النصوص في لغة PHP
👨‍🎓 معلومات الطالب
الاسم: عمرو نبيل عبدالآله محمد
التخصص: تقنية المعلومات
المجموعة: 2

🔵 دوال المصفوفات في PHP مع أمثلة عملية
🔹 الإضافة والحذف
php
// array_push() - إضافة عناصر إلى نهاية المصفوفة
$nums = [1, 2];
array_push($nums, 3, 4); // إضافة 3 و 4
print_r($nums); // النتيجة: [1, 2, 3, 4]

// array_pop() - حذف آخر عنصر من المصفوفة وإرجاعه
$names = ["Ali", "Sara", "Mona"];
$last = array_pop($names); // يحذف Mona
print_r($names); // النتيجة: ["Ali", "Sara"]

// array_unshift() - إضافة عنصر إلى بداية المصفوفة
$colors = ["Blue", "Red"];
array_unshift($colors, "Green"); // إضافة Green
print_r($colors); // النتيجة: ["Green", "Blue", "Red"]

// array_shift() - حذف أول عنصر من المصفوفة
$items = ["banana", "apple", "mango"];
$first = array_shift($items); // يحذف banana
print_r($items); // النتيجة: ["apple", "mango"]
🔹 البحث
php
// in_array() - البحث عن قيمة داخل المصفوفة
$result = in_array("Ali", ["Ahmed", "Ali", "Sara"]); // يرجع true

// array_search() - إرجاع مفتاح العنصر
$key = array_search("red", ["blue", "red", "green"]); // يرجع 1
🔹 الفرز
php
// sort() - ترتيب تصاعدي
$nums = [3, 1, 2];
sort($nums); // النتيجة: [1, 2, 3]

// rsort() - ترتيب تنازلي
$nums = [3, 1, 2];
rsort($nums); // النتيجة: [3, 2, 1]

// asort() - ترتيب حسب القيمة مع الاحتفاظ بالمفتاح
$ages = ["Ali" => 25, "Sara" => 20, "Mona" => 30];
asort($ages); // النتيجة: ["Sara"=>20, "Ali"=>25, "Mona"=>30]

// ksort() - ترتيب حسب المفتاح
$ages = ["Ali" => 25, "Sara" => 20, "Mona" => 30];
ksort($ages); // النتيجة: ["Ali"=>25, "Mona"=>30, "Sara"=>20]
🔹 التعامل مع أجزاء المصفوفة
php
// array_slice() - قص جزء من المصفوفة
$arr = ["a", "b", "c", "d"];
$part = array_slice($arr, 1, 2); // النتيجة: ["b", "c"]

// array_splice() - إزالة/استبدال جزء من المصفوفة
$arr = [1, 2, 3, 4];
array_splice($arr, 1, 2, [5, 6]); // النتيجة: [1, 5, 6, 4]
🔹 الدمج والتحويل
php
// array_merge() - دمج المصفوفات
$a = [1, 2];
$b = [3, 4];
$c = array_merge($a, $b); // النتيجة: [1, 2, 3, 4]

// array_combine() - دمج مفاتيح وقيم في مصفوفة واحدة
$keys = ["name", "age"];
$values = ["Ali", 25];
$result = array_combine($keys, $values); // النتيجة: ["name"=>"Ali", "age"=>25]

// implode() - تحويل مصفوفة إلى نص
$array = ["Ali", "Sara", "Mona"];
$text = implode("-", $array); // النتيجة: "Ali-Sara-Mona"

// explode() - تحويل نص إلى مصفوفة
$text = "Ali,Sara,Mona";
$array = explode(",", $text); // النتيجة: ["Ali", "Sara", "Mona"]
🔹 معلومات حول المصفوفة
php
// count() - عدد العناصر
$count = count([1, 2, 3]); // الناتج: 3

// array_keys() - جلب جميع المفاتيح
$keys = array_keys(["name" => "Ali", "age" => 25]); // النتيجة: ["name", "age"]

// array_values() - جلب جميع القيم
$values = array_values(["name" => "Ali", "age" => 25]); // النتيجة: ["Ali", 25]
🔹 عمليات متقدمة
php
// array_map() - تطبيق دالة على كل عنصر
$numbers = [1, 2, 3];
$squared = array_map(function($n) { return $n * $n; }, $numbers); // النتيجة: [1, 4, 9]

// array_filter() - تصفية المصفوفة
$numbers = [1, 2, 3, 4, 5];
$even = array_filter($numbers, function($n) { return $n % 2 == 0; }); // النتيجة: [2, 4]

// array_reduce() - تقليل عناصر المصفوفة لقيمة واحدة
$numbers = [1, 2, 3, 4];
$sum = array_reduce($numbers, function($carry, $item) { return $carry + $item; }); // النتيجة: 10

// array_unique() - إزالة العناصر المكررة
$numbers = [1, 2, 2, 3, 3, 3];
$unique = array_unique($numbers); // النتيجة: [1, 2, 3]

// array_reverse() - عكس ترتيب عناصر المصفوفة
$arr = [1, 2, 3];
$rev = array_reverse($arr); // النتيجة: [3, 2, 1]
🔵 دوال النصوص في PHP مع أمثلة عملية
🔹 معالجة الحروف
php
// strlen() - طول النص
$length = strlen("Hello"); // 5

// strtoupper() - تحويل إلى حروف كبيرة
$upper = strtoupper("hello"); // HELLO

// strtolower() - تحويل إلى حروف صغيرة
$lower = strtolower("HELLO"); // hello

// ucfirst() - أول حرف كبير
$result = ucfirst("hello world"); // Hello world

// lcfirst() - أول حرف صغير
$result = lcfirst("Hello world"); // hello world

// ucwords() - أول حرف كبير لكل كلمة
$result = ucwords("hello world"); // Hello World
🔹 البحث
php
// strpos() - إيجاد أول ظهور لكلمة
$position = strpos("Hello World", "World"); // النتيجة: 6

// strrpos() - إيجاد آخر ظهور
$position = strrpos("hello world hello", "hello"); // النتيجة: 12

// str_contains() - هل يحتوي النص على كلمة؟
$result = str_contains("Hello World", "World"); // true

// str_starts_with() - هل يبدأ النص بكلمة؟
$result = str_starts_with("Hello World", "Hello"); // true

// str_ends_with() - هل ينتهي بكلمة؟
$result = str_ends_with("Hello World", "World"); // true
🔹 القص والتقسيم
php
// substr() - قص جزء من النص
$part = substr("abcdef", 1, 3); // bcd

// explode() - تحويل نص إلى مصفوفة حسب فاصل
$array = explode(",", "Ali,Sara,Mona"); // ["Ali", "Sara", "Mona"]

// implode() - تحويل مصفوفة إلى نص
$text = implode("-", ["Ali", "Sara", "Mona"]); // Ali-Sara-Mona
🔹 الاستبدال
php
// str_replace() - استبدال كلمة
$result = str_replace("world", "Ali", "Hello world"); // Hello Ali

// preg_replace() - استبدال باستخدام Regex
$result = preg_replace("/\d+/", "number", "I have 123 apples"); // I have number apples
🔹 إزالة المسافات
php
// trim() - حذف المسافات من الطرفين
$clean = trim("   Hello   "); // "Hello"

// ltrim() - حذف مسافات اليسار
$clean = ltrim("   Hello"); // "Hello"

// rtrim() - حذف مسافات اليمين
$clean = rtrim("Hello   "); // "Hello"
🔹 دوال إضافية مهمة
php
// str_repeat() - تكرار النص
$result = str_repeat("Hello", 3); // HelloHelloHello

// str_pad() - إضافة حشوة للنص
$result = str_pad("Hello", 10, "*"); // Hello*****

// str_shuffle() - خلط أحرف النص عشوائياً
$result = str_shuffle("Hello"); // مثال: "leHlo"

// str_word_count() - عد الكلمات في النص
$count = str_word_count("Hello World"); // 2

// str_split() - تقسيم النص إلى مصفوفة أحرف
$chars = str_split("Hello"); // ["H", "e", "l", "l", "o"]
