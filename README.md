# React Firebase: render props
React components for Firebase, using render props

```
yarn add react-firebase-renderprops
```

### Example React Native
```jsx harmony
<Firebase
  config={config.firebaseConfig}
  render={firebase => (
    <FirebaseReference
      firebase={firebase}
      paths={'blog/posts'}
      render={refBlogPosts => (
        <FirebaseQuery
          on
          reference={refBlogPosts}
          limitToLast={20}
          render={posts => (
            <View>
              {posts && posts.map(post => <Text>{post.title}</Text>)}
            </View>
          )}
        />
      )}
    />          
  )}
/>
```



 