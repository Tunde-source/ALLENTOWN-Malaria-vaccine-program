# ALLENTOWN-Malaria-vaccine-program
A program that helps people go for  malaria vaccine easily with not much of time wasting
# Allen Town Malaria Vaccination Tracker

A simple Python command-line tool, built with Object-Oriented Programming, that helps health workers in Allen Town (Freetown, Sierra Leone) track malaria vaccine doses and see which children still need to complete their course.

**Course:** PROG211 Object-Oriented Programming 1, Limkokwing University of Creative Technology
**Author:** <your name and student ID>

## Problem
Malaria vaccines require a full four-dose course (three doses plus a booster). On paper registers it is hard to see who has started, who is in progress and who has finished. This tool records doses per child and quickly lists those who are not yet fully vaccinated.

## Features
- Add anonymous child records (ID and age group only)
- Record doses for the RTS,S/AS01 (Mosquirix) or R21/Matrix-M malaria vaccine
- Enforce a complete course: no more than 4 doses, and the same vaccine for the whole course
- Show all records
- List children who are not fully vaccinated
- Show vaccination information (doses required and schedule)

## How to Run
Requires Python 3.8+ and no external libraries.

```bash
git clone <your-repo-url>
cd vaccination_tracker
python vaccination_tracker.py
```

## Example Usage
```
=== Allen Town Malaria Vaccination Programme ===
1. Add patient record
2. Record dose
3. Show all records
4. List not fully vaccinated
5. Show vaccination info
6. Exit
Select an option: 2
Patient ID: AT001
  1. RTS,S/AS01 (Mosquirix)
  2. R21/Matrix-M
Choose vaccine number: 1
AT001: dose recorded for RTS,S/AS01 (Mosquirix) (1/4).

Select an option: 4

--- Not Fully Vaccinated ---
ID: AT001 | Age group: 5-11 months | Doses: RTS,S/AS01 (Mosquirix) 1/4
ID: AT002 | Age group: 12-23 months | Doses: no doses yet
```
<!-- Replace with your own real output after running the program -->

## OOP Concepts Used
| Concept | Where |
|---|---|
| Classes and objects | `Vaccine`, `Patient` |
| Attributes | `patient_id`, `age_group`, `vaccine`, `doses_received`, `name`, `doses_required`, `schedule` |
| Object interaction | `Patient.record_dose(vaccine)` uses a `Vaccine` object |
| Instance methods | `record_dose()`, `is_fully_vaccinated()`, `display_info()` |
| Class method | `Patient.from_tuple()` |
| Static method | `Patient.is_valid_id()` |
| Data structure | Dictionary `registry` (ID to Patient object) |
| Tuple (optional) | `Patient.AGE_GROUPS` and the input to `from_tuple()` |

## Digital Public Goods (DPG) Alignment
- **Open source:** the code is public on GitHub under the MIT Licence, so anyone can use, study and adapt it.
- **Privacy-respecting:** no names, phone numbers, addresses or other personal data are stored. Only an anonymous ID (e.g. AT001) and a broad age group are used.
- **Inclusive and accessible:** a plain text menu works on low-spec computers and screen readers, with no internet or login needed. Messages use simple language.
- **Modular and reusable:** `Vaccine` and `Patient` are separate classes. New vaccines, age groups or communities can be added without changing the logic.
- **Do no harm:** input validation rejects invalid IDs, duplicate IDs, unknown patients, extra doses and vaccine switching.

## Limitations and Future Work
- Data is held in memory only and is lost on exit. A future version could save to a local CSV or JSON file, still using anonymous IDs only.
- The vaccine schedules shown are general guidance. Always follow the schedule given by the local health authority.
- Future features: booster reminders and support for more health programmes.

## Licence
MIT Licence
