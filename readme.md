## 1.What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
- **getElementById("id")** => প্রদত্ত আইডি অনুসারে ১টি উপাদান পুনরায় সংযুক্ত করুন।
- **getElementsByClassName("class")** => প্রদত্ত ক্লাস সহ সমস্ত উপাদান নির্বাচন করে, HTMLCollection ফেরত দিন।
- **querySelector("css-selector")** => css নির্বাচক হিসাবে প্রথম উপাদানটি ফেরত দিন
- **querySelectorAll("css-selector")** => সমস্ত mached css নির্বাচক হিসাবে NodeList ফেরত দিন

---

## 2. How do you create and insert a new element into the DOM?

- **getElementById("id")** => প্রদত্ত আইডি অনুসারে ১টি উপাদান পুনরায় সংযুক্ত করুন।
- **getElementsByClassName("class")** => প্রদত্ত ক্লাস সহ সমস্ত উপাদান নির্বাচন করে, HTMLCollection ফেরত দিন।
- **querySelector("css-selector")** => css নির্বাচক হিসাবে প্রথম উপাদানটি ফেরত দিন
- **querySelectorAll("css-selector")** => সমস্ত mached css নির্বাচক হিসাবে NodeList ফেরত দিন

---

## 3. What is Event Bubbling and how does it work?
- event rises child to parent
---

- ** Event Bubbling মানে: কোনো child element-এ event ঘটলে সেই event ধাপে ধাপে তার parent → grandparent → document পর্যন্ত propagate হয়।

- **Default behavior: click করলে event প্রথমে target element এ যাবে, তারপর তার parent, তারপর body ইত্যাদি।

---

## 4. What is Event Delegation in JavaScript? Why is it useful?
```js
document.getElementById("list").addEventListener("click", function (e) {
  if(e.target.tagName === "li"){
    console.log("Clicked:", e.target.textContent);
  }
});
```

- প্যারেন্টে একজন শ্রোতা যোগ করা হয়, এবং যখন ইভেন্টটি বুদবুদ হয়ে যায়, তখন লক্ষ্যটি পরীক্ষা করা হয়।

- কেন প্রয়োজন → প্রতিটি সন্তানের জন্য পৃথক শ্রোতা যোগ করার পরিবর্তে, পিতামাতার একজন শ্রোতা সব পরিচালনা করতে পারে। কর্মক্ষমতা উন্নত করে এবং গতিশীল উপাদানগুলির জন্যও কাজ করে।

---

## 5. What is the difference between preventDefault() and stopPropagation() methods?
- **preventDefault()** => এলিমেন্টের ডিফল্ট অ্যাকশন বন্ধ করে (যেমন, ফর্ম সাবমিট, লিঙ্ক রিডাইরেক্ট)।
- **stopPropagation()** => ইভেন্টটিকে প্যারেন্ট এলিমেন্টে বুদবুদ হতে বাধা দেয়।