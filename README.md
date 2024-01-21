# alisop stores
يمكن التعليق وتوجيه ملاحظات لعلي شوب بكل شفافية 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>صفحة التعليقات</title>
</head>
<body>
    <h1>تعليقات الجمهور</h1>
    
    <form id="commentForm">
        <label for="username">اسم المستخدم:</label>
        <input type="text" id="username" name="username" required><br>
        
        <label for="comment">التعليق:</label>
        <textarea id="comment" name="comment" rows="4" required></textarea><br>
        
        <button type="button" onclick="submitComment()">نشر التعليق</button>
    </form>

    <div id="commentsSection">
        <!-- ستظهر التعليقات هنا -->
    </div>

    <script>
        function submitComment() {
            const username = document.getElementById("username").value;
            const commentText = document.getElementById("comment").value;

            if (username && commentText) {
                const commentDiv = document.createElement("div");
                commentDiv.innerHTML = `<strong>${username}:</strong> ${commentText}`;

                document.getElementById("commentsSection").appendChild(commentDiv);

                // يمكنك إضافة المزيد من التعليقات هنا

                // يمكنك إضافة رمز لحفظ التعليقات في localStorage للحفاظ عليها بين الزيارات
            } else {
                alert("الرجاء ملء جميع الحقول");
            }
        }
    </script>
</body>
</html>
