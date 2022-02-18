# LessonTrackerSchema
This repo outlines the schema for LessonTracker 3.0 

# API Docs

Table of Contents

- [Users](#users)
- [User Profiles](#user-profiles)

- [Lessons](#lessons)
- [Lesson Students](#lesson-students)

- [Assignments](#assignments)
- [Student Assignments](#students-assignments)

- [Instruments](#instruments)
- [Student Instruments](#student-instruments)


<a id="users"></a>
## Users
> I think to differentiant 'teachers' and 'students' there can be a `userType` field
> For this 'user' table, keep only account/login/security stuff here. Profile / viewable data should be kept on the profile.

```javascript
{
  userId: number,
  createdAt: Date
}
```

<a id="user-profiles"></a>
## User Profiles
> This separate table for the profile hold all viewable data

```javascript
{
  userId: string,
  name: string,
}
```

<a id="lessons"></a>
## Lessons 


```javascript
{
  lessonId: number,
  teacherId: number,
  startTime: Date,
  duration: number, // durationMinutes ( 30 ) ? durationHours ( 0.5 )?
  description: string

  createdAt: Date,
}
```

<a id="lesson-students"></a>
## Lesson Students

```javascript
{
  lessonId: number,
  studentId: number
}
```

<a id="assignments"></a>
## Assignments

> Are assignments associated with lesson(s)?
> What will the teacher user see?


```
{
}
```

<a id="student-assignments"></a>
## Student Assignment

- Will there be a date to track when the student viewed their assignment?
- Can a single assignement be given to multiple students that belong to differnet lessons?

```
{
}
```

<a id="instruments"></a>
## Instruments

```javascript
{
  instrumentId: number,
  name: string    // "guitar", "bass guitar", "piano", etc
}
```


<a id="student-instruments"></a>
## Student Instruments

```javascript
{
  instrumentId: number,
  studentId: number,
  experienceYears: number
}
```
