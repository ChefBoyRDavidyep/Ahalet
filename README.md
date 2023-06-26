# Ahalet
[Table("Users")] public class User {     [Key, Identity]     public int Id { get; set; }      public string ReadOnly => "test"; // because don't have set      public string Name { get; set; }      public int AddressId { get; set; }      [LeftJoin("Cars", "Id", "UserId")]     public List&lt;Car> Cars { get; set; }
