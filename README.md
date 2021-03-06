# PagerIndicator
[ ![Download](https://api.bintray.com/packages/lyndonchin/maven/pagerindicator/images/download.svg?version=0.0.2) ](https://bintray.com/lyndonchin/maven/pagerindicator/0.0.2/link)

Pager (especially for ViewPager) indicator in two styles: circle & fraction.

## Demo

circle | fraction
--- | ---
<img src="art/art_circular.jpeg" width="300px"> | <img src="art/art_numberic.jpeg" width="300px">

## Dependency

```groovy
implementation 'me.liangfei:pagerindicator:0.0.2'
```

## Usage

Two attributes are provided:
* `app:indicator_type` = [fraction | circle].
* `app:indicator_spacing` works only for the circle type indicator.

**Step 1: add `PageIndicator` to the bottom of the ViewPager.**

```xml
<merge xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto">

    <androidx.viewpager.widget.ViewPager
        android:id="@+id/pager"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />

    <me.liangfei.indicator.PagerIndicator
        android:id="@+id/indicator"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout_marginBottom="20dp"
        android:layout_marginLeft="20dp"
        android:layout_marginStart="20dp"
        android:gravity="bottom|center_horizontal"
        app:indicator_spacing="5dp"
        app:indicator_type="fraction" />
</merge>
```

**Step 2: pass the ViewPager instance to the PagerIndicator instance.**

```kotlin
val pageIndicator = findViewById(R.id.indicator);
pageIndicator.setViewPager(pager);
```

You can just take `PageIndicator` as a normal view to make your layout, because it extends `LinearLayout`.

Check the [app](app) module for more details.

## dependencies
* [Fresco](https://github.com/facebook/fresco)

## 欢迎关注我的微信公众号（Chinese only）
<img width="300px" src="https://cdn.nlark.com/yuque/0/2019/png/124977/1552294534293-9ae5a46a-df3c-4020-8096-a05534f53a0b.png">
