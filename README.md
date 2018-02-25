# Job Notes

Keep on top of your next contract or perm role with notes on the go

## Motivation

I was inundated with contract and perm roles just before starting my most recent contract. What would have been useful is if there was a way I could keep on top of the interviews, the recruiters, and interviewers - especially while on the tube and on the go. Job Notes is there to solve that problem.

## Stack

Front End:
- React
- Apollo Client

Back End:
- Go
- Postgres
- GraphQL

## Design

### Stories

As a software engineer I'd like to see and manage a list of potential future gigs so I can plan my interviews and not be in a state of brain fog.

As a London Underground commuter, I'd like to read and manage notes for upcoming interviews on my mobile as it's likely I won't get a seat and can't wade through printouts without falling.

### Data

```
type Company {
	id: ID!
	name: String!
	address: String
}

type Recruiter {
	id: ID!
	name: String!
	telephone: Int,
	email: String
}

enum Rating {
	HOT
	DEFAULT
}

enum Status {
	OPEN
	CLOSED_ACCEPTED
	CLOSED_I_DECLINED
	CLOSED_THEY_DECLINED
}

type Opportunity {
	id: ID!
	company: Company
	recruiter: Recruiter
	note: String
	rating: Rating
	status: Status
}
```

### UI
