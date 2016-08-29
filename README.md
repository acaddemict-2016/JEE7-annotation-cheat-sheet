# JEE7-annotation-cheat-sheet
A handy dandy overview of all the annotations that were crammed into our heads. Please fill out!


## Bean Validation

 Annotation    |  Explanation
---------------|-------------------------------------------------
 @NotNull      |
 @Min          |
 @Max          |


## CDI

Annotation    |  Explanation
--------------|-------------------------------------------------
@Inject       | No more `new`! Let the server create objects for you.
@PersistenceContext | A JPA annotation to inject the Entity Manager. Allows to give more configuration options.


## Entities

 Annotation    |  Explanation
---------------|-------------------------------------------------
 @Entity       | Turn a java bean into an entity that persists in the database.
 @Id           | Indicates which attribute of an entity is used as the id.
 @GeneratedValue | Often used in conjunction with `@Id`. It makes the database generate a value for this field.
 


## EJB's

Annotation    |  Explanation
--------------|-------------------------------------------------
@Stateless    |
@Stateful     |
@Singleton    |
@MessageDriven |
@Remote       |
@Local        |



## Web Services

Annotation    |  Explanation
--------------|-------------------------------------------------
@WebService   | Transforms a bean into a web service.
@WebParam     | Optional. Allows you to rename method parameters in SOAP messages.
@WebMethod    | Optional. Allows you to rename method names in SOAP messages.
@XmlRootElement | Used on entities to allow turning them into XML.
@XmlAttribute | Used on an entity's getters to tweak XML output.
@XmlElement   | Used on an entity's getters to tweak XML output.
