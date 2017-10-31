---
id: version-0.20-view
title: view
original_id: view
---
<a id="content"></a><table width="100%"><tbody><tr><td><h1><a class="anchor" name="view"></a>View <a class="hash-link" href="#view">#</a></h1></td><td style="text-align:right;"><a target="_blank" href="https://github.com/facebook/react-native/blob/master/Libraries/Components/View/View.js">Edit on GitHub</a></td></tr></tbody></table><div><div><p>The most fundamental component for building UI, <code>View</code> is a
container that supports layout with flexbox, style, some touch handling, and
accessibility controls, and is designed to be nested inside other views and
to have 0 to many children of any type. <code>View</code> maps directly to the native
view equivalent on whatever platform React is running on, whether that is a
<code>UIView</code>, <code>&lt;div&gt;</code>, <code>android.view</code>, etc.  This example creates a <code>View</code> that
wraps two colored boxes and custom component in a row with padding.</p><div class="prism language-javascript">&lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>flexDirection<span class="token punctuation">:</span> <span class="token string">'row'</span><span class="token punctuation">,</span> height<span class="token punctuation">:</span> <span class="token number">100</span><span class="token punctuation">,</span> padding<span class="token punctuation">:</span> <span class="token number">20</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
  &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>backgroundColor<span class="token punctuation">:</span> <span class="token string">'blue'</span><span class="token punctuation">,</span> flex<span class="token punctuation">:</span> <span class="token number">0.3</span><span class="token punctuation">}</span><span class="token punctuation">}</span> <span class="token operator">/</span><span class="token operator">&gt;</span>
  &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>backgroundColor<span class="token punctuation">:</span> <span class="token string">'red'</span><span class="token punctuation">,</span> flex<span class="token punctuation">:</span> <span class="token number">0.5</span><span class="token punctuation">}</span><span class="token punctuation">}</span> <span class="token operator">/</span><span class="token operator">&gt;</span>
  &lt;MyCustomComponent <span class="token punctuation">{</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span>customProps<span class="token punctuation">}</span> <span class="token operator">/</span><span class="token operator">&gt;</span>
&lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span></div><p><code>View</code>s are designed to be used with <code>StyleSheet</code>s for clarity and
performance, although inline styles are also supported.</p></div><h3><a class="anchor" name="props"></a>Props <a class="hash-link" href="#props">#</a></h3><div class="props"><div class="prop"><h4 class="propTitle"><a class="anchor" name="accessibilitylabel"></a>accessibilityLabel <span class="propType">string</span> <a class="hash-link" href="#accessibilitylabel">#</a></h4><div><p>Overrides the text that's read by the screen reader when the user interacts
with the element. By default, the label is constructed by traversing all the
children and accumulating all the Text nodes separated by space.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="accessible"></a>accessible <span class="propType">bool</span> <a class="hash-link" href="#accessible">#</a></h4><div><p>When true, indicates that the view is an accessibility element. By default,
all the touchable elements are accessible.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onaccessibilitytap"></a>onAccessibilityTap <span class="propType">function</span> <a class="hash-link" href="#onaccessibilitytap">#</a></h4><div><p>When <code>accessible</code> is true, the system will try to invoke this function
when the user performs accessibility tap gesture.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onlayout"></a>onLayout <span class="propType">function</span> <a class="hash-link" href="#onlayout">#</a></h4><div><p>Invoked on mount and layout changes with</p><p>  {nativeEvent: { layout: {x, y, width, height}}}.</p><p>This event is fired immediately once the layout has been calculated, but
the new layout may not yet be reflected on the screen at the time the
event is received, especially if a layout animation is in progress.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onmagictap"></a>onMagicTap <span class="propType">function</span> <a class="hash-link" href="#onmagictap">#</a></h4><div><p>When <code>accessible</code> is true, the system will invoke this function when the
user performs the magic tap gesture.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onmoveshouldsetresponder"></a>onMoveShouldSetResponder <span class="propType">function</span> <a class="hash-link" href="#onmoveshouldsetresponder">#</a></h4></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onmoveshouldsetrespondercapture"></a>onMoveShouldSetResponderCapture <span class="propType">function</span> <a class="hash-link" href="#onmoveshouldsetrespondercapture">#</a></h4></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onrespondergrant"></a>onResponderGrant <span class="propType">function</span> <a class="hash-link" href="#onrespondergrant">#</a></h4><div><p>For most touch interactions, you'll simply want to wrap your component in
<code>TouchableHighlight</code> or <code>TouchableOpacity</code>. Check out <code>Touchable.js</code>,
<code>ScrollResponder.js</code> and <code>ResponderEventPlugin.js</code> for more discussion.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onrespondermove"></a>onResponderMove <span class="propType">function</span> <a class="hash-link" href="#onrespondermove">#</a></h4></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onresponderreject"></a>onResponderReject <span class="propType">function</span> <a class="hash-link" href="#onresponderreject">#</a></h4></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onresponderrelease"></a>onResponderRelease <span class="propType">function</span> <a class="hash-link" href="#onresponderrelease">#</a></h4></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onresponderterminate"></a>onResponderTerminate <span class="propType">function</span> <a class="hash-link" href="#onresponderterminate">#</a></h4></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onresponderterminationrequest"></a>onResponderTerminationRequest <span class="propType">function</span> <a class="hash-link" href="#onresponderterminationrequest">#</a></h4></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onstartshouldsetresponder"></a>onStartShouldSetResponder <span class="propType">function</span> <a class="hash-link" href="#onstartshouldsetresponder">#</a></h4></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onstartshouldsetrespondercapture"></a>onStartShouldSetResponderCapture <span class="propType">function</span> <a class="hash-link" href="#onstartshouldsetrespondercapture">#</a></h4></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="pointerevents"></a>pointerEvents <span class="propType">enum('box-none', 'none', 'box-only', 'auto')</span> <a class="hash-link" href="#pointerevents">#</a></h4><div><p>In the absence of <code>auto</code> property, <code>none</code> is much like <code>CSS</code>'s <code>none</code>
value. <code>box-none</code> is as if you had applied the <code>CSS</code> class:</p><div class="prism language-javascript"><span class="token punctuation">.</span>box<span class="token operator">-</span>none <span class="token punctuation">{</span>
  pointer<span class="token operator">-</span>events<span class="token punctuation">:</span> none<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<span class="token punctuation">.</span>box<span class="token operator">-</span>none <span class="token operator">*</span> <span class="token punctuation">{</span>
  pointer<span class="token operator">-</span>events<span class="token punctuation">:</span> all<span class="token punctuation">;</span>
<span class="token punctuation">}</span></div><p><code>box-only</code> is the equivalent of</p><div class="prism language-javascript"><span class="token punctuation">.</span>box<span class="token operator">-</span>only <span class="token punctuation">{</span>
  pointer<span class="token operator">-</span>events<span class="token punctuation">:</span> all<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<span class="token punctuation">.</span>box<span class="token operator">-</span>only <span class="token operator">*</span> <span class="token punctuation">{</span>
  pointer<span class="token operator">-</span>events<span class="token punctuation">:</span> none<span class="token punctuation">;</span>
<span class="token punctuation">}</span></div><p>But since <code>pointerEvents</code> does not affect layout/appearance, and we are
already deviating from the spec by adding additional modes, we opt to not
include <code>pointerEvents</code> on <code>style</code>. On some platforms, we would need to
implement it as a <code>className</code> anyways. Using <code>style</code> or not is an
implementation detail of the platform.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="removeclippedsubviews"></a>removeClippedSubviews <span class="propType">bool</span> <a class="hash-link" href="#removeclippedsubviews">#</a></h4><div><p>This is a special performance property exposed by RCTView and is useful
for scrolling content when there are many subviews, most of which are
offscreen. For this property to be effective, it must be applied to a
view that contains many subviews that extend outside its bound. The
subviews must also have overflow: hidden, as should the containing view
(or one of its superviews).</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="style"></a>style <span class="propType">style</span> <a class="hash-link" href="#style">#</a></h4><div class="compactProps"><div class="prop"><h6 class="propTitle"><a href="docs/flexbox.html#proptypes">Flexbox...</a></h6></div><div class="prop"><h6 class="propTitle"><a href="docs/shadowproptypesios.html#style">ShadowPropTypesIOS#style...</a></h6></div><div class="prop"><h6 class="propTitle"><a href="docs/transforms.html#proptypes">Transforms...</a></h6></div><div class="prop"><h6 class="propTitle">backfaceVisibility <span class="propType">enum('visible', 'hidden')</span> </h6></div><div class="prop"><h6 class="propTitle">backgroundColor <span class="propType"><a href="docs/colors.html">color</a></span> </h6></div><div class="prop"><h6 class="propTitle">borderBottomColor <span class="propType"><a href="docs/colors.html">color</a></span> </h6></div><div class="prop"><h6 class="propTitle">borderBottomLeftRadius <span class="propType">number</span> </h6></div><div class="prop"><h6 class="propTitle">borderBottomRightRadius <span class="propType">number</span> </h6></div><div class="prop"><h6 class="propTitle">borderBottomWidth <span class="propType">number</span> </h6></div><div class="prop"><h6 class="propTitle">borderColor <span class="propType"><a href="docs/colors.html">color</a></span> </h6></div><div class="prop"><h6 class="propTitle">borderLeftColor <span class="propType"><a href="docs/colors.html">color</a></span> </h6></div><div class="prop"><h6 class="propTitle">borderLeftWidth <span class="propType">number</span> </h6></div><div class="prop"><h6 class="propTitle">borderRadius <span class="propType">number</span> </h6></div><div class="prop"><h6 class="propTitle">borderRightColor <span class="propType"><a href="docs/colors.html">color</a></span> </h6></div><div class="prop"><h6 class="propTitle">borderRightWidth <span class="propType">number</span> </h6></div><div class="prop"><h6 class="propTitle">borderStyle <span class="propType">enum('solid', 'dotted', 'dashed')</span> </h6></div><div class="prop"><h6 class="propTitle">borderTopColor <span class="propType"><a href="docs/colors.html">color</a></span> </h6></div><div class="prop"><h6 class="propTitle">borderTopLeftRadius <span class="propType">number</span> </h6></div><div class="prop"><h6 class="propTitle">borderTopRightRadius <span class="propType">number</span> </h6></div><div class="prop"><h6 class="propTitle">borderTopWidth <span class="propType">number</span> </h6></div><div class="prop"><h6 class="propTitle">borderWidth <span class="propType">number</span> </h6></div><div class="prop"><h6 class="propTitle">opacity <span class="propType">number</span> </h6></div><div class="prop"><h6 class="propTitle">overflow <span class="propType">enum('visible', 'hidden')</span> </h6></div><div class="prop"><h6 class="propTitle"><span class="platform">android</span>elevation <span class="propType">number</span> <div><p>(Android-only) Sets the elevation of a view, using Android's underlying
<a href="https://developer.android.com/training/material/shadows-clipping.html#Elevation" target="_blank">elevation API</a>.
This adds a drop shadow to the item and affects z-order for overlapping views.
Only supported on Android 5.0+, has no effect on earlier versions.</p></div></h6></div></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="testid"></a>testID <span class="propType">string</span> <a class="hash-link" href="#testid">#</a></h4><div><p>Used to locate this view in end-to-end tests. NB: disables the 'layout-only
view removal' optimization for this view!</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="accessibilitycomponenttype"></a><span class="platform">android</span>accessibilityComponentType <span class="propType">AccessibilityComponentType</span> <a class="hash-link" href="#accessibilitycomponenttype">#</a></h4><div><p>Indicates to accessibility services to treat UI component like a
native one. Works for Android only.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="accessibilityliveregion"></a><span class="platform">android</span>accessibilityLiveRegion <span class="propType">enum('none', 'polite', 'assertive')</span> <a class="hash-link" href="#accessibilityliveregion">#</a></h4><div><p>Indicates to accessibility services whether the user should be notified
when this view changes. Works for Android API &gt;= 19 only.
See <a href="http://developer.android.com/reference/android/view/View.html#attr_android:accessibilityLiveRegion">http://developer.android.com/reference/android/view/View.html#attr_android:accessibilityLiveRegion</a>
for references.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="collapsable"></a><span class="platform">android</span>collapsable <span class="propType">bool</span> <a class="hash-link" href="#collapsable">#</a></h4><div><p>Views that are only used to layout their children or otherwise don't draw
anything may be automatically removed from the native hierarchy as an
optimization. Set this property to <code>false</code> to disable this optimization and
ensure that this View exists in the native view hierarchy.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="importantforaccessibility"></a><span class="platform">android</span>importantForAccessibility <span class="propType">enum('auto', 'yes', 'no', 'no-hide-descendants')</span> <a class="hash-link" href="#importantforaccessibility">#</a></h4><div><p>Controls how view is important for accessibility which is if it
fires accessibility events and if it is reported to accessibility services
that query the screen. Works for Android only.
See <a href="http://developer.android.com/reference/android/R.attr.html#importantForAccessibility">http://developer.android.com/reference/android/R.attr.html#importantForAccessibility</a>
for references.
Possible values:
'auto' - The system determines whether the view is important for accessibility -
   default (recommended).
'yes' - The view is important for accessibility.
'no' - The view is not important for accessibility.
'no-hide-descendants' - The view is not important for accessibility,
   nor are any of its descendant views.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="needsoffscreenalphacompositing"></a><span class="platform">android</span>needsOffscreenAlphaCompositing <span class="propType">bool</span> <a class="hash-link" href="#needsoffscreenalphacompositing">#</a></h4><div><p>Whether this view needs to rendered offscreen and composited with an alpha
in order to preserve 100% correct colors and blending behavior. The default
(false) falls back to drawing the component and its children with an alpha
applied to the paint used to draw each element instead of rendering the full
component offscreen and compositing it back with an alpha value. This default
may be noticeable and undesired in the case where the View you are setting
an opacity on has multiple overlapping elements (e.g. multiple overlapping
Views, or text and a background).</p><p>Rendering offscreen to preserve correct alpha behavior is extremely
expensive and hard to debug for non-native developers, which is why it is
not turned on by default. If you do need to enable this property for an
animation, consider combining it with renderToHardwareTextureAndroid if the
view <strong>contents</strong> are static (i.e. it doesn't need to be redrawn each frame).
If that property is enabled, this View will be rendered off-screen once,
saved in a hardware texture, and then composited onto the screen with an alpha
each frame without having to switch rendering targets on the GPU.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="rendertohardwaretextureandroid"></a><span class="platform">android</span>renderToHardwareTextureAndroid <span class="propType">bool</span> <a class="hash-link" href="#rendertohardwaretextureandroid">#</a></h4><div><p>Whether this view should render itself (and all of its children) into a
single hardware texture on the GPU.</p><p>On Android, this is useful for animations and interactions that only
modify opacity, rotation, translation, and/or scale: in those cases, the
view doesn't have to be redrawn and display lists don't need to be
re-executed. The texture can just be re-used and re-composited with
different parameters. The downside is that this can use up limited video
memory, so this prop should be set back to false at the end of the
interaction/animation.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="accessibilitytraits"></a><span class="platform">ios</span>accessibilityTraits <span class="propType">AccessibilityTraits, [AccessibilityTraits]</span> <a class="hash-link" href="#accessibilitytraits">#</a></h4><div><p>Provides additional traits to screen reader. By default no traits are
provided unless specified otherwise in element</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="shouldrasterizeios"></a><span class="platform">ios</span>shouldRasterizeIOS <span class="propType">bool</span> <a class="hash-link" href="#shouldrasterizeios">#</a></h4><div><p>Whether this view should be rendered as a bitmap before compositing.</p><p>On iOS, this is useful for animations and interactions that do not
modify this component's dimensions nor its children; for example, when
translating the position of a static view, rasterization allows the
renderer to reuse a cached bitmap of a static view and quickly composite
it during each frame.</p><p>Rasterization incurs an off-screen drawing pass and the bitmap consumes
memory. Test and measure when using this property.</p></div></div></div></div><div><table width="100%"><tbody><tr><td><h3><a class="anchor" name="examples"></a>Examples <a class="hash-link" href="#examples">#</a></h3></td><td style="text-align:right;"><a target="_blank" href="https://github.com/facebook/react-native/blob/master/Examples/UIExplorer/ViewExample.js">Edit on GitHub</a></td></tr></tbody></table><div class="prism language-javascript"><span class="token string">'use strict'</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> Platform <span class="token operator">=</span> <span class="token function">require<span class="token punctuation">(</span></span><span class="token string">'Platform'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> React <span class="token operator">=</span> <span class="token function">require<span class="token punctuation">(</span></span><span class="token string">'react-native'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> <span class="token punctuation">{</span>
  StyleSheet<span class="token punctuation">,</span>
  Text<span class="token punctuation">,</span>
  View<span class="token punctuation">,</span>
<span class="token punctuation">}</span> <span class="token operator">=</span> React<span class="token punctuation">;</span>
<span class="token keyword">var</span> TouchableWithoutFeedback <span class="token operator">=</span> <span class="token function">require<span class="token punctuation">(</span></span><span class="token string">'TouchableWithoutFeedback'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> styles <span class="token operator">=</span> StyleSheet<span class="token punctuation">.</span><span class="token function">create<span class="token punctuation">(</span></span><span class="token punctuation">{</span>
  box<span class="token punctuation">:</span> <span class="token punctuation">{</span>
    backgroundColor<span class="token punctuation">:</span> <span class="token string">'#527FE4'</span><span class="token punctuation">,</span>
    borderColor<span class="token punctuation">:</span> <span class="token string">'#000033'</span><span class="token punctuation">,</span>
    borderWidth<span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> ViewBorderStyleExample <span class="token operator">=</span> React<span class="token punctuation">.</span><span class="token function">createClass<span class="token punctuation">(</span></span><span class="token punctuation">{</span>
  <span class="token function">getInitialState<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">{</span>
      showBorder<span class="token punctuation">:</span> <span class="token boolean">true</span>
    <span class="token punctuation">}</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">(</span>
      &lt;TouchableWithoutFeedback onPress<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>_handlePress<span class="token punctuation">}</span><span class="token operator">&gt;</span>
        &lt;View<span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>
            borderWidth<span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            borderRadius<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span>
            borderStyle<span class="token punctuation">:</span> <span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>showBorder <span class="token operator">?</span> <span class="token string">'dashed'</span> <span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            padding<span class="token punctuation">:</span> <span class="token number">5</span>
          <span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
            &lt;Text style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>fontSize<span class="token punctuation">:</span> <span class="token number">11</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
              Dashed border style
            &lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
          &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>
            marginTop<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span>
            borderWidth<span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            borderRadius<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span>
            borderStyle<span class="token punctuation">:</span> <span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>showBorder <span class="token operator">?</span> <span class="token string">'dotted'</span> <span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            padding<span class="token punctuation">:</span> <span class="token number">5</span>
          <span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
            &lt;Text style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>fontSize<span class="token punctuation">:</span> <span class="token number">11</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
              Dotted border style
            &lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
          &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
      &lt;<span class="token operator">/</span>TouchableWithoutFeedback<span class="token operator">&gt;</span>
    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  <span class="token function">_handlePress<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState<span class="token punctuation">(</span></span><span class="token punctuation">{</span>showBorder<span class="token punctuation">:</span> <span class="token operator">!</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>showBorder<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

exports<span class="token punctuation">.</span>title <span class="token operator">=</span> <span class="token string">'&lt;View&gt;'</span><span class="token punctuation">;</span>
exports<span class="token punctuation">.</span>description <span class="token operator">=</span> <span class="token string">'Basic building block of all UI, examples that '</span> <span class="token operator">+</span>
  <span class="token string">'demonstrate some of the many styles available.'</span><span class="token punctuation">;</span>

exports<span class="token punctuation">.</span>displayName <span class="token operator">=</span> <span class="token string">'ViewExample'</span><span class="token punctuation">;</span>
exports<span class="token punctuation">.</span>examples <span class="token operator">=</span> <span class="token punctuation">[</span>
  <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Background Color'</span><span class="token punctuation">,</span>
    render<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> <span class="token punctuation">(</span>
        &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>backgroundColor<span class="token punctuation">:</span> <span class="token string">'#527FE4'</span><span class="token punctuation">,</span> padding<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
          &lt;Text style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>fontSize<span class="token punctuation">:</span> <span class="token number">11</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
            Blue background
          &lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
      <span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span> <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Border'</span><span class="token punctuation">,</span>
    render<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> <span class="token punctuation">(</span>
        &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>borderColor<span class="token punctuation">:</span> <span class="token string">'#527FE4'</span><span class="token punctuation">,</span> borderWidth<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span> padding<span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
          &lt;Text style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>fontSize<span class="token punctuation">:</span> <span class="token number">11</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>5px blue border&lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
      <span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span> <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Padding/Margin'</span><span class="token punctuation">,</span>
    render<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> <span class="token punctuation">(</span>
        &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>borderColor<span class="token punctuation">:</span> <span class="token string">'#bb0000'</span><span class="token punctuation">,</span> borderWidth<span class="token punctuation">:</span> <span class="token number">0.5</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">[</span>styles<span class="token punctuation">.</span>box<span class="token punctuation">,</span> <span class="token punctuation">{</span>padding<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">}</span><span class="token punctuation">]</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
            &lt;Text style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>fontSize<span class="token punctuation">:</span> <span class="token number">11</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>5px padding&lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
          &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">[</span>styles<span class="token punctuation">.</span>box<span class="token punctuation">,</span> <span class="token punctuation">{</span>margin<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">}</span><span class="token punctuation">]</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
            &lt;Text style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>fontSize<span class="token punctuation">:</span> <span class="token number">11</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>5px margin&lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
          &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">[</span>styles<span class="token punctuation">.</span>box<span class="token punctuation">,</span> <span class="token punctuation">{</span>margin<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span> padding<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span> alignSelf<span class="token punctuation">:</span> <span class="token string">'flex-start'</span><span class="token punctuation">}</span><span class="token punctuation">]</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
            &lt;Text style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>fontSize<span class="token punctuation">:</span> <span class="token number">11</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
              5px margin and padding<span class="token punctuation">,</span>
            &lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
            &lt;Text style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>fontSize<span class="token punctuation">:</span> <span class="token number">11</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
              widthAutonomous<span class="token operator">=</span><span class="token boolean">true</span>
            &lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
          &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
      <span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span> <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Border Radius'</span><span class="token punctuation">,</span>
    render<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> <span class="token punctuation">(</span>
        &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>borderWidth<span class="token punctuation">:</span> <span class="token number">0.5</span><span class="token punctuation">,</span> borderRadius<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span> padding<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
          &lt;Text style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>fontSize<span class="token punctuation">:</span> <span class="token number">11</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
            Too much use of `borderRadius` <span class="token punctuation">(</span>especially large radii<span class="token punctuation">)</span> on
            anything which is scrolling may result <span class="token keyword">in</span> dropped frames<span class="token punctuation">.</span>
            Use sparingly<span class="token punctuation">.</span>
          &lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
      <span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span> <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Border Style'</span><span class="token punctuation">,</span>
    render<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> &lt;ViewBorderStyleExample <span class="token operator">/</span><span class="token operator">&gt;</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span> <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Circle with Border Radius'</span><span class="token punctuation">,</span>
    render<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> <span class="token punctuation">(</span>
        &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>borderRadius<span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span> borderWidth<span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span> width<span class="token punctuation">:</span> <span class="token number">20</span><span class="token punctuation">,</span> height<span class="token punctuation">:</span> <span class="token number">20</span><span class="token punctuation">}</span><span class="token punctuation">}</span> <span class="token operator">/</span><span class="token operator">&gt;</span>
      <span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span> <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Overflow'</span><span class="token punctuation">,</span>
    render<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> <span class="token punctuation">(</span>
        &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>flexDirection<span class="token punctuation">:</span> <span class="token string">'row'</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
          &lt;View
            style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>
              width<span class="token punctuation">:</span> <span class="token number">95</span><span class="token punctuation">,</span>
              height<span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span>
              marginRight<span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span>
              marginBottom<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span>
              overflow<span class="token punctuation">:</span> <span class="token string">'hidden'</span><span class="token punctuation">,</span>
              borderWidth<span class="token punctuation">:</span> <span class="token number">0.5</span><span class="token punctuation">,</span>
            <span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
            &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>width<span class="token punctuation">:</span> <span class="token number">200</span><span class="token punctuation">,</span> height<span class="token punctuation">:</span> <span class="token number">20</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
              &lt;Text<span class="token operator">&gt;</span>Overflow hidden&lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
            &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
          &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>width<span class="token punctuation">:</span> <span class="token number">95</span><span class="token punctuation">,</span> height<span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span> marginBottom<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span> borderWidth<span class="token punctuation">:</span> <span class="token number">0.5</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
            &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>width<span class="token punctuation">:</span> <span class="token number">200</span><span class="token punctuation">,</span> height<span class="token punctuation">:</span> <span class="token number">20</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
              &lt;Text<span class="token operator">&gt;</span>Overflow visible&lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
            &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
          &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
      <span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span> <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Opacity'</span><span class="token punctuation">,</span>
    render<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> <span class="token punctuation">(</span>
        &lt;View<span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>opacity<span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>&lt;Text<span class="token operator">&gt;</span>Opacity <span class="token number">0</span>&lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>&lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>opacity<span class="token punctuation">:</span> <span class="token number">0.1</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>&lt;Text<span class="token operator">&gt;</span>Opacity <span class="token number">0.1</span>&lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>&lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>opacity<span class="token punctuation">:</span> <span class="token number">0.3</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>&lt;Text<span class="token operator">&gt;</span>Opacity <span class="token number">0.3</span>&lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>&lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>opacity<span class="token punctuation">:</span> <span class="token number">0.5</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>&lt;Text<span class="token operator">&gt;</span>Opacity <span class="token number">0.5</span>&lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>&lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>opacity<span class="token punctuation">:</span> <span class="token number">0.7</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>&lt;Text<span class="token operator">&gt;</span>Opacity <span class="token number">0.7</span>&lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>&lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>opacity<span class="token punctuation">:</span> <span class="token number">0.9</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>&lt;Text<span class="token operator">&gt;</span>Opacity <span class="token number">0.9</span>&lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>&lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
          &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>opacity<span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>&lt;Text<span class="token operator">&gt;</span>Opacity <span class="token number">1</span>&lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>&lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
      <span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
<span class="token punctuation">]</span><span class="token punctuation">;</span></div></div><div class="docs-prevnext"><a class="docs-next" href="docs/viewpagerandroid.html#content">Next →</a></div>