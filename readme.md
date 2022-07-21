**1.Get the number of characters in a string**

Getting the count of characters is a useful utility in many cases, we can use it to get the number of spaces followed by words, or this can be used to get the count of a certain delimiter in a string.

`const characterCount = (str, char) => str.split(char).length - 1`

The idea is simple, we split the string using the passed parameter char and get the length of the returned array. Since each time the string is split, there is one more than the splitter; so subtract 1 and we have a single line of characterCount .

**2. Check if the object is empty**

Checking for nullability of an object is actually more difficult than it looks, even if the object is null, every time checking if the object is equal to {} will return false.

Fortunately, the one-liner below is exactly what we want.

`const isEmpty = obj => Reflect.ownKeys(obj).length === 0 && obj.constructor === Object`

In this line, we check if the key length of the object is equal to 0, and if the passed argument is an actual object.

**3. Wait for a while before executing**

In this line, we’re going to dirty our code with some asynchronous programming. The idea is simple, when running the code, if you want to wait a certain amount of time, here is the wait single line:

`const wait = async (time) => new Promise((resolve) => setTimeout(resolve, milliseconds));`

In the await one-liner, we create a promise and resolve it using the setTimeout function after a given amount of time.

**4. Get the daily difference between two dates**

When developing a web application, dates are often the most confusing part of implementing because there are many concepts that can easily be miscalculated.

This is a powerful one-liner to calculate the difference in days between two dates. But there is more to do, as I did, you can create your own one-liners to calculate month, year differences, etc.

`const daysBetween = (date1, date2) => Math.ceil(Math.abs(date1 - date2) / (1000 * 60 * 60 * 24));`

The logic behind this one-liner is easy to understand. When subtracting two dates, the return value is the difference in milliseconds, to convert milliseconds to days, we have to divide it by milliseconds, seconds, minutes, and hours.

**5. Redirect to another URL**

If you’ve ever created a real website, I’m sure you’ve encountered authentication logic. For example, non-admin users should not be able to access the /admin route. If the user tries, then, you have to redirect them to another URL.

This one-liner is exactly what I mentioned above, but I think you can find more use cases.

`const redirect = url => location.href = url;`

location is a method of the global window object, and setting the href property behaves the same as if the user clicked a link.

**6. Check for touch support on your device**

With more and more devices that can connect to the internet, the need to create a responsive website also increases. Twenty years ago, developers should have considered the desktop version of a website, but today more than 70% of web traffic comes from touch mobile devices. So it is a very important concept to take some action based on the touch support of the device.

`const touchSupported = () => ('ontouchstart' in window || DocumentTouch && document instanceof DocumentTouch);`

In this line, we are checking if the document supports the touchstart event.

**7. Insert HTML string after element**

Using JavaScript to update the DOM is a very common thing when developing web applications. There are some basic ways to get the job done, but when things get complicated, it’s hard to overcome.
This is a one-liner that injects an HTML string right after the HTML element. After a few minutes of thinking and googling, I believe you can find previous versions of this one-liner.

`const insertHTMLAfter = (html, el) => el.insertAdjacentHTML('afterend', html);`

**8. Randomly arrange arrays**

Shuffling a set of data in development is a common situation that you can come across at any time, unfortunately there is no built-in shuffle method for arrays in JavaScript.

However, here is a shuffle one-liner you can use every day:

`const shuffle = arr => arr.sort(() => Math.random() > 0.5);`

It utilizes the sorting method of arrays to randomly sort before or after the previous element of the array.

**9. Get selected text on web page**

Browsers have a built-in method called getSelection on the global window object. Using this method, you can create a single line that returns highlighted or selected text on a web page.

`const getSelectedText = () => window.getSelection().toString();`

**10. Get a random boolean value**

When developing, especially when writing game code, sometimes we want to take random actions. In these cases, the one-liner below is very handy.

`const getRandomBoolean = () => Math.random() >= 0.5;`

The single line of code above has a 50/50 chance of returning true or false. Because the probability of generating a random number greater than 0.5 is equal to the probability of becoming smaller.

However, if, for example, you wanted to get a random boolean value with a probability of 70%, then you could simply change 0.5 to 0.3 and so on.

**11. Calculate the average of an array**

The mean of an array can be calculated in a number of ways. But the logic is the same for all, we have to get the sum of the array and its length; then, give the average by division.

`const average = (arr) => arr.reduce((a, b) => a + b) / arr.length;`
