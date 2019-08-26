### beanmother
---
https://github.com/keepcosmos/beanmother

```java
ObjectMother objectMoher = ObjectMother.getInstance();

@Test
public void testSingleObject() {
  Book book = objectMother.bear("book", Book.class);
  Author author = objectMother.bear("author", Author.class);
}

@Test
public void testMultipleObjects() {
  List<Author> authors = objectMother.bear("author", Author.class, 10);
}

public class MyScriptRunner implements ScriptRunner {

  @Override
  public Object run(ScriptFragment scriptFragment) {
    return any;
  }
  
  @Override
  public boolean canHandle(ScriptFragment scriptFragment) {
    return scriptFragment.getMethodName.equal("myname");
  }
}

```

```yml
# test/resources/fixtures/publishing.yml

book: &book
  title: ${faker.book.title}
  language: en
  publishedAt: ${faker.date.between('2000-01-01', '2010-01-01')}

author:
  id: ${sequence.number}
  name: Ernest Hemingway
  instoduction: ${faker.lorem.paragraph}
  birth: July 21, 1899
  gender: MALE
  works:
    - <<: *book
    - <<: *book
    - <<: *book
```

```
```


