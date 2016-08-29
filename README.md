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
@PostConstruct | It's dangerous to initialize variables of an injectable bean in a constructor. Use this annotation to mark a method that is run after construction. This method can be used to do setup.
@Qualifier    | If the variable you want to inject is an abstract class or an interface, polymorphism will screw up the injection. To fix this, create an annotation with a name for each of the subclasses and use `@Qualifier` when implementing the annotation.
@Alternative  |
@Default      |
@Produces     | Use this to inject things that are otherwise not injectable like strings, collections or classes without default constructor.


## Entities / JPA

 Annotation    |  Explanation
---------------|-------------------------------------------------
 @Entity       | Turn a java bean into an entity that persists in the database.
 @Inheritance  |
 @Id           | Indicates which attribute of an entity is used as the id.
 @Version      |
 @GeneratedValue | Often used in conjunction with `@Id`. It makes the database generate a value for this field.
 @EmbeddedId   | Used if the id of an entity is another class. This is used for composite keys. Requires `@Embeddable` on the class that represents the key.
 @Embeddable   | Use this to store the information of a class that's stored as variable into the entity's database table.
 @Embeddable   | Makes a java bean embeddable into an entity. The fields of this embeddable class will appear in the database table of the entity it is embedded in.
 @Valid        | Used together with `@Embedded` and `@EmbeddedId`. Makes sure that upon entity validation, the embedded class is also validated.
 @Column       | Used to give configuration parameters about a field's column in the database. Useful options are `table` to create a separate table for a variable, `nullable` to make columns mandatory and `updatable`, which does exactly what you think it does.
 @Temporal     | Store a field as a date. Give a `TemporalType` as option.
 @Enumerated   | Store an enum value either as integer with `EnumType.ORDINAL` or as a string with `EnumType.STRING`.
 @Transient    | Don't store a field in the database.
 @Basic        |
 @Lob          |
 @ElementCollection | Similar to `@Embeddable`, but then for when you have a collection of `@Embeddable` objects. It creates a new table with a foreign key to the entity the `@Embeddable` is linked to. You can configure the newly created table with `@CollectionTable`.
 @CollectionTable | Configure the table created with `@ElementCollection`.
 @OneToMany     |
 @ManyToOne     |
 @OneToOne      |
 @ManyToMany    |
 @JoinColumn    |
 @JoinColumns   |



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
