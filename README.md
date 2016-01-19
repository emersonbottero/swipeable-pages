Copyright (c) 2014 Hassan Hayat <hassan.hayat7@gmail.com>
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the 'Software'), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

Provides horizontally swipeable pages. Based in https://github.com/TheSeamau5/swipe-pages

The `swipeable-pages` element is given a certain width and height
through CSS and then each individual `swipeable-page` will automatically take of the full size of the parent element. This means that the children elements are assumed to all have the exact same size which they all derive from the `swipeable-pages`
element.
you must indicate the page-count
###Example:
    <swipeable-pages class="flex horizontal layout" selected="{{selectedtab}}" page-count="[[tabs.length]]">
      <div>Hey I'm page 0</div>
      <div><h1>Hi, I'm on page 1</h1></div>
      <div><p>I am page 2 and I totally rock!</p></div>
    </swipeable-pages>
Swiping left moves to the next page while swiping right moves to the previous page.
This behavior is very typical on mobile applications.
The key to this element is that when swiping, the page follows your finger
horizontally so as to give the user immediate feedback that he/she is swiping
between pages.
Pages only transition when the swipe gesture has crossed a certain threshold
which is exposed by the `threshold` attribute.
###Example:
    <swipeable-pages threshold = '0.5' page-count="3">
    </swipeable-pages>
By setting the `threshold` to 0.5, you ensure that the page will only transition
if the swipe gesture has crossed half the `swipeable-pages` width horizontally.
`threshold` accepts values between 0 and 1.
A `threshold` value of 0 implies that any swipe gesture will cause a page
transition. A `threshold` value of 1 implies that no page transition is possible
as you must cross more that the entire size of the `swipeable-pages` element horizontally
which is impossible given that the size of the `swipeable-pages` element is well-defined.
@class swipeable-pages
@blurb Provides horizontally swipeable pages.
@status alpha
