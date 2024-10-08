# shoppe

# فروشگاه آنلاین

این پروژه یک فروشگاه آنلاین است که با استفاده از **React** و **TypeScript** توسعه یافته است. ساختار پروژه به صورت ماژولار طراحی شده تا هم از نظر خوانایی و هم از نظر قابلیت نگهداری بهینه باشد.

## ساختار پوشه‌ها

### توضیحات پوشه‌ها

#### 1. `assets/`

این پوشه شامل تمامی فایل‌های استاتیک پروژه است، مانند تصاویر، فونت‌ها و آیکون‌ها. ساختار آن به شکل زیر است:

- `images/` برای نگهداری تصاویر.
- `fonts/` برای فونت‌های سفارشی.
- `icons/` برای آیکون‌های سفارشی پروژه.

#### 2. `components/`

این پوشه شامل تمامی کامپوننت‌های پروژه است. کامپوننت‌ها به چند زیرشاخه تقسیم شده‌اند:

- **`common/`**: شامل اجزای عمومی و قابل استفاده مجدد مانند `Button`، `Input`، و `Modal`.
- **`layout/`**: کامپوننت‌های مربوط به ساختار کلی صفحات مانند `Header`، `Footer`، و `Sidebar`.
- **`product/`**: کامپوننت‌های مرتبط با نمایش محصولات مانند `ProductCard` و `ProductList`.
- **`cart/`**: کامپوننت‌های مربوط به سبد خرید، مانند `CartItem` و `CartSummary`.

#### 3. `hooks/`

تمامی هوک‌های سفارشی که برای استفاده مجدد از عملکردهای مختلف پروژه طراحی شده‌اند در این پوشه قرار می‌گیرند. برای مثال:

- **`useCart.js`**: برای مدیریت سبد خرید.
- **`useProduct.js`**: برای مدیریت اطلاعات محصولات.

#### 4. `pages/`

این پوشه شامل صفحات اصلی برنامه است:

- **`HomePage.js`**: صفحه اصلی فروشگاه.
- **`ProductPage.js`**: صفحه نمایش جزئیات محصول.
- **`CartPage.js`**: صفحه سبد خرید.
- **`CheckoutPage.js`**: صفحه پرداخت.

#### 5. `services/`

این پوشه مسئول مدیریت درخواست‌های API است. تمامی توابع مرتبط با فراخوانی API‌ها در اینجا قرار می‌گیرند:

- **`api.js`**: برای مدیریت ارتباط با سرور و ارسال درخواست‌های HTTP مثل دریافت لیست محصولات، ثبت سفارش و...

#### 6. `context/`

پوشه‌ای برای مدیریت `Context API`، برای نگهداری حالت‌های سراسری (Global State) مثل سبد خرید و احراز هویت:

- **`CartContext.js`**: مدیریت وضعیت سبد خرید.
- **`AuthContext.js`**: مدیریت وضعیت احراز هویت.

#### 7. `store/`

این پوشه برای مدیریت state با استفاده از ابزارهای مدیریت state مانند **Redux** در نظر گرفته شده است. هر ماژول حالت در فایل جداگانه‌ای تعریف شده است:

- **`cartSlice.js`**: برای مدیریت وضعیت سبد خرید.
- **`productSlice.js`**: برای مدیریت وضعیت محصولات.

#### 8. `utils/`

این پوشه شامل توابع و ابزارهای کمکی است که در بخش‌های مختلف پروژه استفاده می‌شوند. به عنوان مثال:

- `formatCurrency.js`: فرمت کردن قیمت‌ها به صورت صحیح.
- `calculateTotal.js`: محاسبه جمع کل سبد خرید.

#### 9. `styles/`

این پوشه شامل استایل‌های سراسری پروژه است. در اینجا می‌توانید فایل‌های SCSS یا CSS خود را قرار دهید:

- **`global.scss`**: استایل‌های کلی و متغیرهای CSS برای استفاده در کل پروژه.

#### 10. `App.js`

این فایل نقطه ورودی اصلی برنامه شما است و مسئول مدیریت مسیرها (Routes) و ساختار کلی پروژه است.

#### 11. `index.js`

فایل ورودی اصلی پروژه است که `App` را رندر کرده و برنامه شما را شروع می‌کند.

#### 12. `routes.js`

تمامی مسیرهای برنامه در این فایل مدیریت می‌شوند. از این فایل برای تعیین صفحات مختلف و مسیرهای URL استفاده می‌شود.

## نصب و راه‌اندازی

برای نصب پروژه مراحل زیر را دنبال کنید:

1. ابتدا مخزن را کلون کنید:

   ```bash
   git clone https://github.com/username/project-name.git

   ```

2. سپس به پوشه پروژه بروید:

   ```bash
    cd project-name

   ```

3. وابستگی‌ها را نصب کنید:

   ```bash
    npm install

   ```

4. برای راه‌اندازی برنامه در حالت توسعه:
   ```bash
    npm start
   ```

### توضیحات کلی:

- در این فایل، تمام بخش‌های پروژه به دقت توضیح داده شده‌اند.
- نصب و راه‌اندازی پروژه نیز به شکل دستوراتی ساده ارائه شده تا توسعه‌دهندگان جدید بتوانند به راحتی پروژه را راه‌اندازی کنند.
- به مدیریت state و ارتباط با API نیز اشاره شده که از اهمیت بالایی برخوردار است.

شما می‌توانید این فایل را با تغییرات جزئی مربوط به پروژه خودتان در گیت‌هاب قرار دهید تا دیگران بتوانند به راحتی پروژه را درک و از آن استفاده کنند.
