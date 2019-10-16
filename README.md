# JSR380-Spring-Validation
Spring Validation 


jsr380spring5validation:

step 1:

 

pom.xml:

 

<dependency>

    <groupId>javax.validation</groupId>

    <artifactId>validation-api</artifactId>

    <version>2.0.0.Final</version>

</dependency>

 

standard JSR annotation:

 

@NotNull – validates that the annotated property value is not null

@AssertTrue – validates that the annotated property value is true

@Size – validates that the annotated property value has a size between the attributes min and max; can be applied to String, Collection, Map, and array properties

@Min – vValidates that the annotated property has a value no smaller than the value attribute

@Max – validates that the annotated property has a value no larger than the value attribute

@Email – validates that the annotated property is a valid email address

 

found in the JSR are:

 

@NotEmpty – validates that the property is not null or empty; can be applied to String, Collection, Map or Array values

@NotBlank – can be applied only to text values and validated that the property is not null or whitespace

@Positive and @PositiveOrZero – apply to numeric values and validate that they are strictly positive, or positive including 0

@Negative and @NegativeOrZero – apply to numeric values and validate that they are strictly negative, or negative including 0

@Past and @PastOrPresent – validate that a date value is in the past or the past including the present; can be applied to date types including those added in Java 8

@Future and @FutureOrPresent – validates that a date value is in the future, or in the future including the present

 

public class User {

    @NotNull(message = "Name cannot be null")

    private String name;

    @AssertTrue

    private boolean working;

    @Size(min = 10, max = 200, message

      = "About Me must be between 10 and 200 characters")

    private String aboutMe;

    @Min(value = 18, message = "Age should not be less than 18")

    @Max(value = 150, message = "Age should not be greater than 150")

    private int age;

    @Email(message = "Email should be valid")

    private String email;

    // standard setters and getters

}
