### Entity Framework

Seeding data best to drop and recreate database and then seed.

dotnet ef database drop
dotnet ef database update
dotnet run

### Usefull website

https://caniuse.com/
https://docs.microsoft.com/en-us/aspnet/core/fundamentals/environments?view=aspnetcore-2.2

### Random JSON data generator tool

===========
Snippet for JSON Generator site at https://www.json-generator.com/
===========

[
  '{{repeat(5)}}',
  {
    Username: '{{firstName("female")}}',
    Gender: 'female',
    DateOfBirth: '{{date(new Date(1950,0,1), new Date(1999, 11, 31), "YYYY-MM-dd")}}',
    Password: 'password',
    KnownAs: function(){ return this.Username; },
    Created: '{{date(new Date(2017,0,1), new Date(2017, 7, 31), "YYYY-MM-dd")}}',
    LastActive: function(){return this.Created; },
    Introduction: '{{lorem(1, "paragraphs")}}',
    LookingFor: '{{lorem(1, "paragraphs")}}',
    Interests: '{{lorem(1, "sentences")}}',
    City: '{{city()}}',
    Country: '{{country()}}',
    Photos: [
        {
          url: function(num) {
          return 'https://randomuser.me/api/portraits/women/' + num.integer(1,99) + '.jpg';
        },
        isMain: true,
        description: '{{lorem()}}'
      }
    ]
  }
]


===========
Snippet for NEXT JSON Generator site at https://next.json-generator.com
===========



[
  {
    'repeat(5)': {
    Username: '{{firstName("female")}}',
    Gender: 'female',
    DateOfBirth: '{{date(new Date(1950,0,1), new Date(1999, 11, 31), "YYYY-MM-dd")}}',
    Password: 'password',
    KnownAs: function(){ return this.Username; },
    Created: '{{date(new Date(2017,0,1), new Date(2017, 7, 31), "YYYY-MM-dd")}}',
    LastActive: function(){return this.Created; },
    Introduction: '{{lorem(1, "paragraphs")}}',
    LookingFor: '{{lorem(1, "paragraphs")}}',
    Interests: '{{lorem(1, "sentences")}}',
    City: '{{city()}}',
    Country: '{{country()}}',
    Photos: [
        {
          url: function(num) {
          return 'https://randomuser.me/api/portraits/women/' + num.integer(1,99) + '.jpg';
        },
        isMain: true,
        description: '{{lorem()}}'
      }
    ]
  }
 }
]